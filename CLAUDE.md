# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A single-person CV pipeline: Markdown source files are rendered to styled PDFs via WeasyPrint. The Markdown files double as the human-readable content *and* the input to PDF generation. There are two CV variants, each a `README*.md` → `CV*.pdf` pair:

- `README.md` → `CV.pdf` — the short/primary CV
- `README_FULL.md` → `CV_FULL.pdf` — the full/long CV

Editing the CV means editing the Markdown, then regenerating the corresponding PDF. The generated PDFs are committed to the repo (they're linked from GitHub raw URLs inside `README.md`).

## Commands

Uses [uv](https://docs.astral.sh/uv/) for dependency and script running (Python >=3.13).

```bash
# Build the PDFs (run both after editing either README)
uv run scripts/md_to_pdf.py README.md --output CV.pdf --css styles/pdf.css
uv run scripts/md_to_pdf.py README_FULL.md --output CV_FULL.pdf --css styles/pdf.css

# Live preview in the browser (auto-opens; edit Markdown + refresh to see changes)
uv run scripts/dev_preview.py --port 8765 --markdown README.md --css styles/pdf.css
```

`main.py` is a placeholder entrypoint and is not part of the pipeline.

## Architecture

Both scripts share the same rendering approach so preview and PDF stay visually consistent:

- **`scripts/md_to_pdf.py`** — converts one Markdown file to PDF. Renders Markdown → HTML with the `python-markdown` extensions `extra, fenced_code, toc, sane_lists, smarty`, wraps it in a minimal HTML document, then feeds it to WeasyPrint with an external stylesheet. `base_url` is set to the Markdown file's parent dir so relative asset paths resolve. If `--css` is omitted or missing, it falls back to an inline `DEFAULT_CSS` constant defined in the file.
- **`scripts/dev_preview.py`** — a Flask dev server that renders the *same* Markdown with the *same* extension list, links `styles/pdf.css`, and serves it with caching disabled so a browser refresh always reflects the latest edit. Use it to debug print layout before committing to a PDF rebuild.
- **`styles/pdf.css`** — the single source of print styling (A4, `@page` margins, point-based font sizes). This is the file to edit for PDF appearance; the inline `DEFAULT_CSS` in `md_to_pdf.py` is only a fallback and should generally be kept in sync or ignored.

The two markdown extension lists (in each script) must be kept identical for preview and PDF output to match.

## WeasyPrint system dependencies

WeasyPrint needs native libraries (Pango, Cairo, HarfBuzz). On Linux install them via the system package manager; on macOS Homebrew you may need to export `DYLD_FALLBACK_LIBRARY_PATH`. See `.env.example` for the exact package names and the macOS env var, then `set -a; source .env; set +a` before running.

## Notes

- Several source materials (`CV_PLAN.md`, other people's CVs, `docs/ai/`) are gitignored and local-only — don't expect them in the repo.

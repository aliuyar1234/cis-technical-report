# LaTeX / PDF export (Overleaf)

This folder is provided so you can generate a PDF from the docs-only paper using an online LaTeX editor (e.g., Overleaf), without changing any reported numbers or identifiers.

## Files

- `main.tex`: minimal LaTeX wrapper that renders the Markdown paper via the `markdown` package.
- `PAPER.md`: a copy of `docs/PAPER.md` for LaTeX rendering.

## Overleaf steps

1. Create a new Overleaf project.
2. Upload the contents of this `latex/` folder (`main.tex`, `PAPER.md`, `README.md`).
3. Set the main file to `main.tex` (if Overleaf doesn't auto-detect it).
4. Compile and download the PDF.

If Overleaf reports that the `markdown` package is unavailable, tell me the exact error and I’ll provide a fallback `main.tex` that does not depend on it.


# Build and Repository Rules

## Build

Work from the `Notes/` directory:

```bash
latexmk -pdf -interaction=nonstopmode -halt-on-error -file-line-error main.tex
```

The build must end with `EXIT=0` and produce `main.pdf`.

## Expected output

- Current page count: **115 pages** (may change when a chapter is expanded; record the new count in the decision log).
- Current known warning: one overfull hbox in the bibliography, caused by the `mixup` entry.
- Any additional overfull hbox, undefined reference, or missing citation is a regression and must be fixed before committing.

## Repository layout

```text
Notes/
  main.tex                 document assembly and bibliography
  structure.tex            global styles, boxes, chapter headings
  bibliography.bib         citation database
  Chapters/                one .tex file per chapter
  Pictures/                figures and the FDS exercise PDF
  KnowledgeBase/           this folder
  main.pdf                 tracked build artifact
```

## Rules

- Do not add `\begin{document}` or `\end{document}` to a chapter file.
- Do not delete `Pictures/FDS_Exercises.pdf`. It is required by Chapter 1.
- Do not commit auxiliary files listed in `.gitignore` (`*.aux`, `*.log`, `*.toc`, etc.).
- `main.pdf` is tracked; rebuild it before committing so the committed PDF matches the sources.
- Keep image filenames stable. If an image is replaced, update every `\includegraphics` reference in the same commit.
- When a chapter is added, include it in `main.tex` and add its label to `03_Lesson_Map.md`.

## Pre-commit checklist

1. `latexmk` exits with code 0.
2. No new overfull hboxes beyond the known bibliography warning.
3. The table of contents shows the expected chapters and sections.
4. The new or changed pages have been rendered and inspected.
5. `05_Decision_Log.md` is updated if an editorial rule changed.
6. The recap table is present and the old `Chapter Summary and Conceptual Graph` is gone.

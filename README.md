# AML Notes

LaTeX course notes for **Advanced Machine Learning and Computer Vision** (Università La Sapienza).

## Build

From this directory:

```bash
latexmk -pdf -interaction=nonstopmode -halt-on-error -file-line-error main.tex
```

The output is `main.pdf`.

## Editorial standards

All editorial, symbolic, and structural decisions are recorded in [`KnowledgeBase/`](KnowledgeBase/README.md). Read that folder before adding or revising a chapter.

Key rules:

- Lecture slides in `../AML/` are the source of truth.
- Chapters end with `Recap: Key Concepts`, not the old conceptual roadmap.
- The handwritten backpropagation exercise in `Pictures/FDS_Exercises.pdf` is a required part of Chapter 1.
- The symbol standard is proposed but not yet applied globally; do not migrate one chapter in isolation.

## Structure

```text
main.tex                 document assembly and bibliography
structure.tex            global styles, boxes, chapter headings
Chapters/                one .tex file per chapter
Pictures/                figures and the FDS exercise PDF
KnowledgeBase/           editorial and structural standards
bibliography.bib         citation database
```

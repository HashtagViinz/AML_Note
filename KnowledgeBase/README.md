# AML Notes — Knowledge Base

This folder records the editorial, mathematical, and structural standards used in the course notes. Treat every file here as the reference whenever a chapter is added or revised. If a decision changes, update the relevant file and add an entry to `05_Decision_Log.md`; do not leave the standard implicit in a commit message.

If a standard conflicts with an explicit instruction from the author, the author's instruction prevails. Update the standard and record the change in the decision log.

## Index

| File | Purpose |
|---|---|
| `01_Editorial_Standards.md` | Tone, chapter structure, boxes, figures, recap format, and forbidden patterns. |
| `02_Symbol_Standard.md` | Target notation, current usage, and migration rules. |
| `03_Lesson_Map.md` | Mapping between lecture decks and chapters, including ignored and future decks. |
| `04_Coverage_Methodology.md` | How to measure key-concept coverage against the slides. |
| `05_Decision_Log.md` | Chronological record of editorial and structural decisions. |
| `06_Build_and_Repo.md` | Build command, expected warnings, file layout, and repository rules. |
| `07_Chapter_Template.md` | Copy-ready skeleton for a new chapter. |
| `08_Concept_Map.md` | Detailed lecture-concept to book-section mapping, chapter by chapter. |
| `09_Slide_Key_Map.md` | Slide-keyed mapping: each professor slide group to its place in the book. |

## Current status

- Chapters 1--6 have been revised and now end with `Recap: Key Concepts`.
- The symbol standard is a target, not yet applied globally. Do not change symbols in one chapter in isolation.
- The book currently compiles to 115 pages with one known bibliography overfull hbox.
- The handwritten backpropagation exercise (`Pictures/FDS_Exercises.pdf`) is a required part of Chapter 1 and must never be removed.

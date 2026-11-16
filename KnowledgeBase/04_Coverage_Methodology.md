# Coverage Methodology

## Two scores

Coverage is reported with two numbers:

- **Core coverage** — the fraction of technical concepts that a student must understand to follow the lecture and solve its exercises.
- **Raw coverage** — the fraction of all slide items, including history, motivation, repeated title slides, administrative notes, and implementation asides.

The target is **at least 90% core coverage** for Chapters 1--2, and **complete technical coverage** for Chapters 3--6. Raw coverage may be lower; it is a diagnostic, not a goal.

## What counts as a core concept

A core concept is a definition, equation, architecture, training rule, or trade-off that the lecture uses to build the next concept. Examples:

- the convolution formula, padding, stride, and receptive field;
- the LSTM cell-state update and the role of each gate;
- scaled dot-product attention and the reason for the `1/\sqrt{D_k}` factor;
- the MLM loss and the ELECTRA replaced-token objective.

Not core concepts:

- the title slide, the outline slide, and repeated section dividers;
- the lecturer's biography or administrative announcements;
- a list of paper authors without a technical claim;
- a PyTorch API walkthrough that does not introduce a model concept.

## Procedure

1. Extract the slide text with `pdftotext -layout` and list the slide titles.
2. For each slide, write down the technical claim or equation it introduces.
3. Map each claim to a section or subsection in the chapter.
4. Mark it:
   - **Covered** — the chapter states the concept and explains it.
   - **Partial** — the chapter mentions it but does not explain it.
   - **Missing** — the chapter does not mention it.
5. Add or expand the missing and partial items at the lecture's level.
6. Recompute the score and record it in the decision log.

## Verification

- Do not trust `pdftotext` alone for figures, diagrams, or equations embedded as images. Render the relevant PDF pages with `pdftoppm` and inspect them.
- After a revision, check the table of contents, the page count, and the layout of the new pages.
- A concept that appears only in a figure caption does not count as covered; it must be explained in the body text.
- A formula that appears without an explanation of its symbols does not count as covered.

## Reporting

Use a short report at the end of a revision:

```text
Chapter X
Core coverage: NN%
Raw coverage: NN%
Added: ...
Still missing: ...
Known limitations: ...
```

Record the report in `05_Decision_Log.md` and, if the chapter is complete, in the chapter's commit message.

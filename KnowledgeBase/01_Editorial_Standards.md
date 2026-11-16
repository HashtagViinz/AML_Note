# Editorial Standards

## 1. Language and tone

- The notes are written in English, with an academic but readable tone.
- Prefer short, declarative explanations over long narrative paragraphs.
- Explain every formula that appears in the slides. Do not introduce extra derivations unless they are needed to make a lecture concept understandable.
- Keep the mathematical level of the lecture. Do not replace a lecture-level argument with a more advanced one.
- Define a symbol the first time it is used in a chapter. If a symbol has a different meaning in another chapter, say so explicitly.

## 2. Chapter structure

Every technical chapter follows this order:

1. **Introduction** — what problem the chapter solves and why it matters.
2. **Core theory** — definitions, equations, and the intuition behind them.
3. **Worked examples** — at least one concrete numerical or step-by-step example where the lecture provides one.
4. **Practical notes** — training recipes, implementation caveats, or trade-offs that appear in the slides.
5. **`Recap: Key Concepts`** — a table plus one `InsightBox` sentence.
6. **No old-style conceptual roadmap** — the `Chapter Summary and Conceptual Graph` section and its TikZ roadmap are retired.

A chapter must not end with a list of vague "logical connections between nodes". It must end with a compact, self-contained recap that a student can use the night before the exam.

## 3. Boxes

Use the boxes defined in `structure.tex` consistently:

| Box | Use it for |
|---|---|
| `Notebox` | A caveat, a practical warning, or a subtle point that is easy to miss. |
| `keywordbox` | A formal rule, a definition, or a compact set of equations that must stand out. |
| `examplebox` | A worked numerical example or a step-by-step trace. |
| `InsightBox` | The single most important takeaway of a section or of the whole chapter. |

Rules:

- Do not put a full derivation in a box; put it in the body text and use the box for the result.
- Do not use two boxes of the same type back to back without body text between them.
- The final `InsightBox` of a chapter is exactly one sentence.
- Keep boxes short enough to fit on one page with their surrounding text.

## 4. Figures and tables

- Every figure needs a `\caption` and a `\label`, and must be referenced in the text with `Figure~\ref{...}`.
- Prefer the original slide image when it carries the lecture's visual argument.
- Do not crop a figure in a way that removes a label, an axis, or a formula. If the source image already contains a clipped title, trim only the clipped fragment or replace the asset.
- Tables must use `booktabs` (`\toprule`, `\midrule`, `\bottomrule`) and `p{...}` columns for text.
- Table widths should sum to about `0.88\textwidth`; wider tables produce overfull hboxes.

## 5. Recap format

The recap is a table with exactly three columns:

| Concept | Key idea | Formula / rule |
|---|---|---|

- 10--14 rows for a normal chapter.
- The first column is a short noun phrase, the second is one line of intuition, the third is a formula or a compact rule.
- After the table, add one `InsightBox` beginning with `\textbf{The one-sentence version:}`.
- The recap must be understandable without rereading the chapter.

## 6. Forbidden patterns

- Markdown artifacts in `.tex` files: `---`, `**bold**`, backtick code fences.
- The phrase `Chapter Summary and Conceptual Graph`.
- Hand-written `tikzpicture` roadmaps that duplicate the table of contents.
- Removing or replacing the handwritten FDS backpropagation exercise in Chapter 1.
- Introducing a new symbol in one chapter while the rest of the book still uses the old one.
- Copying slide bullet lists verbatim without explaining them.

## 7. Revision workflow

1. Read the slide deck and list its technical concepts.
2. Compare the list with the current chapter and mark each concept as covered, partial, or missing.
3. Add missing concepts at the lecture's level of detail.
4. Replace the old summary with a recap table.
5. Compile and inspect the affected pages as images, not only as text.
6. Update `05_Decision_Log.md` if an editorial rule changed.

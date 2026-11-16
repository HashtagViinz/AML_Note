# Decision Log

Newest entries at the bottom. Each entry records what was decided, why, and whether the decision is fully applied.

| Date | Decision | Rationale | Status |
|---|---|---|---|
| 2026-11-13 | Chapters 1--4 end with `Recap: Key Concepts` (table + one-sentence `InsightBox`) instead of `Chapter Summary and Conceptual Graph`. | The old roadmaps were confusing and duplicated the table of contents. A compact table is easier to revise. | Applied to Chapters 1--4. Chapter 5 still uses the old summary. |
| 2026-11-13 | The handwritten backpropagation exercise in `Pictures/FDS_Exercises.pdf` is mandatory in Chapter 1. | It is the most complete worked backpropagation example in the course materials and the user explicitly requires it. | Applied; do not remove. |
| 2026-11-13 | Chapter 2 distinguishes convolution from cross-correlation and explains the 180-degree kernel flip. | Without the flip, the operation is cross-correlation, not convolution. The distinction was previously hidden in a keyword box. | Applied as Section 2.3.3 and a corrected 2D example. |
| 2026-11-13 | `04_AMLCV_Pytorch_recap.pdf` is ignored. | It is a practical tool tutorial, not a theory lecture. | Applied. |
| 2026-11-13 | Chapter 3 adds Stacked RNNs and an LSTM-versus-GRU comparison. | The slides include a multilayer RNN diagram and the summary explicitly mentions GRU; the chapter covered neither. | Applied. |
| 2026-11-13 | Chapter 4 restores the compact explanations and equations that had been removed by an uncommitted simplification: the `1/\sqrt{D_k}` justification, relative positional encoding, the ViT embedding equation, the MLM loss, and the distillation equations. | The simplified prose was shorter but lost the mathematical content of the slides. Restoring compact equations preserves both readability and coverage. | Applied. |
| 2026-11-13 | Relative positional encoding is a separate subsection in Chapter 4. | The slides devote two slides to it and it is a distinct mechanism from absolute sinusoidal encoding. | Applied. |
| 2026-11-13 | The KnowledgeBase is the authority for future editorial, symbolic, and structural decisions. | Decisions were previously implicit in commits and conversation, which caused regressions. | Applied; keep this log updated. |
| 2026-11-13 | Target symbol standard: `s` for scores, `z` for latents, `\eta` for learning rate, `a_{t,i}` for attention weights, `F` for filter size, `n_\ell` for layers, `n_h` for heads, `T` for tokens, `W_{\text{img}}/H_{\text{img}}` for image dimensions, `c_t^{\text{att}}` for attention context, `N_d` for decoder layers, `M` for masks. | The book currently mixes `z`/`y` for logits, `\alpha`/`\eta` for learning rate, and `K`/`F` for filter size. | Proposed; **not yet applied globally**. Do not migrate one chapter in isolation. |
| 2026-11-13 | Chapter 4 adds the Image Transformer's local self-attention mechanism and a BERT fine-tuning paragraph. | Both are lecture topics that were only mentioned in passing; local attention explains how Transformers handle megapixel images, and fine-tuning completes the pre-training/fine-tuning recipe. | Applied. |
| 2026-11-13 | Chapter 5 DINO section expanded: DINO training details (EMA teacher, stop-gradient, symmetrized loss), DINOv2 (iBOT, KoLeo, PCA visualization), and DINOv3 (scaling pipeline, Gram anchoring, student family, high-resolution adaptation). | The DINO slides 110--116 cover three generations and the original chapter compressed v2/v3 into one paragraph. The pseudocode figure was also mislabeled as a segmentation figure and has been corrected. | Applied. |
| 2026-11-13 | The book must compile cleanly; the only accepted warning is the pre-existing `mixup` bibliography overfull hbox. | New overfull boxes usually indicate a table or figure that is too wide. | Applied; current build has only the known bibliography warning. |
| 2026-11-14 | Chapter 5 recap replaces the old `Chapter Summary and Conceptual Graph`. The comparative SSL table was removed as a float and its content folded into a short comparative paragraph, so the standard recap table remains the only end-of-chapter summary. | The old roadmap and five-column table floated away from their sections and produced near-empty pages. A single recap table matches Chapters 1--4 and keeps the layout stable. | Applied. |
| 2026-11-15 | Created Chapter 6, "Object Detection and Segmentation", from deck 08. DINO self-supervised remains in Chapter 5; the deck only covers DETR, not the DINO detector. Historical and open-source-framework slides were skipped. | The deck is a core lecture and deserves its own chapter. Appending it as Chapter 6 avoids renumbering the completed Chapter 5 and keeps the existing labels stable. | Applied; build is 115 pages. |

## How to add an entry

1. Use the date of the decision, not the date of the commit.
2. State the decision in one sentence.
3. State the reason in one sentence.
4. Mark the status as `Proposed`, `Applied`, `Superseded`, or `Rejected`.
5. If a decision supersedes an older one, say which row it replaces.

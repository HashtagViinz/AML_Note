# Symbol Standard

## Status

This is the **target notation** for the book. It has **not** been applied globally yet. Do not migrate a single chapter in isolation: a partial migration creates inconsistencies between chapters. The migration must be done in one pass, chapter by chapter, followed by a full compile and a notation check.

## Target symbols

| Symbol | Meaning | Notes |
|---|---|---|
| `s` | Scores or logits before Softmax | Replaces the current use of `z` for scores in several chapters. |
| `z` | Latent variable, embedding, or hidden representation | Never use `z` for logits. |
| `\eta` | Learning rate | Replaces `\alpha` in optimization equations. |
| `a_{t,i}` | Attention weight of decoder step `t` on encoder position `i` | Replaces `\alpha_{t,i}`. In self-attention use `a_{i,j}`. |
| `F` | Convolutional filter size | Replaces `K` for the spatial extent in convolution formulas. |
| `n_\ell` | Number of layers | Use `\ell` as the layer index. |
| `n_h` | Number of attention heads | Use `h` as the head index. |
| `T` | Number of tokens or time steps | Keep `t` for a single index. |
| `W_{\text{img}}`, `H_{\text{img}}` | Image width and height | Avoid bare `W`/`H`, which collide with weights and hidden states. |
| `c_t^{\text{att}}` | Attention context vector at step `t` | Distinguishes it from the LSTM cell state `c_t`. |
| `N_d` | Number of decoder layers | `N_e` for encoder layers if needed. |
| `M` | Mask matrix | Entries `0` or `-\infty` before Softmax. |

## Current usage and migration map

| Concept | Current usage in the notes | Target | Migration action |
|---|---|---|---|
| Logits / scores | `z` in Chapter 1; `y` in Chapter 3 | `s` | Rename only during the global pass; update every equation and caption. |
| Latent / embedding | `z` in several places | `z` | Keep, but remove any use of `z` as logits. |
| Learning rate | `\alpha` in Chapter 1 | `\eta` | Rename in text, equations, and recap tables. |
| Attention weights | `\alpha_{t,i}` in Chapter 4 | `a_{t,i}` | Rename together with the attention equations. |
| Filter size | `K` in Chapters 2--3 | `F` | Rename in convolution and receptive-field formulas. |
| Number of layers | `L`, `N` | `n_\ell` | Use `\ell` for the index; keep `L` only for a fixed depth if needed. |
| Number of heads | `H` | `n_h` | `H` is also image height; disambiguate. |
| Image dimensions | `H`, `W` | `H_{\text{img}}`, `W_{\text{img}}` | Rename in vision chapters. |
| Context vector | `c_t` in attention; `c_t` in LSTM | `c_t^{\text{att}}` for attention | Keep `c_t` for the LSTM cell state. |
| Decoder depth | `N` | `N_d` | Rename in Transformer sections. |
| Mask | `M` | `M` | Already consistent. |

## Rules

1. A symbol has exactly one meaning within a chapter.
2. If a symbol must be reused, add a footnote or a parenthetical clarification at the point of reuse.
3. Do not rename a symbol in a single equation; rename every occurrence in the chapter, including captions and tables.
4. After the global migration, add a `Notation` table to the front matter and reference it from the introduction.
5. Until the migration is complete, this file is the authority for *new* text: new sections should use the target symbols even if older sections still use the legacy ones, and the inconsistency must be recorded in the decision log.

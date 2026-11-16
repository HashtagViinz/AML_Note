# Lesson Map

## Source of truth

The lecture slide decks in `AML/` are the source of truth for topic coverage. The notes are not a transcript: they reorganize the slides into a coherent textbook chapter, but they must not omit a technical concept that the slides treat as part of the lecture.

## Current mapping

| Deck | Topic | Destination | Status |
|---|---|---|---|
| `01_AMLCV_intro.pdf` | Course introduction | Not included | Non-technical; intentionally excluded. |
| `02_AMLCV_neural_networks.pdf` | Foundations of deep learning | Chapter 1 | Included and revised. |
| `03_AMLCV_convnets.pdf` | Convolutional networks and computer vision | Chapter 2 | Included and revised. |
| `04_AMLCV_Pytorch_recap.pdf` | PyTorch practical recap | Not included | Ignored by decision; it is a tool tutorial, not a lecture concept. |
| `05_AMLCV_TrainingNN.pdf` | Training neural networks | Chapter 1 (training foundations) + Chapter 2 (data augmentation, transfer learning) | Split by topic; both parts are covered. |
| `06_AML_Sequence_Models_I.pdf` | Sequence models I | Chapter 3 | Included and revised. |
| `07_AML_Sequence_Models_II.pdf` | Sequence models II / Transformers | Chapter 4 | Included and revised. |
| `08_AML_Detection_Segmentation.pdf` | Detection and segmentation | Chapter 6 | Included and revised. |
| `09_AML_SSL.pdf` | Self-supervised learning | Chapter 5 | Included and revised. |
| `10_AML_HyperbolicLearning.pdf` | Hyperbolic learning | Future chapter | Not yet in the manual. |
| `11_AML_GenAI_VAE_GAN.pdf` | Generative AI: VAE and GAN | Future chapter | Not yet in the manual. |

Do not confuse these decks with older versions from a previous year. Update this table if the deck naming changes.

## Chapter labels

| Chapter | Label | File |
|---|---|---|
| 1 | `ch:foundations` | `Chapters/Chapter1.tex` |
| 2 | `ch:convnets` | `Chapters/Chapter2.tex` |
| 3 | `ch:sequence_models` | `Chapters/Chapter3.tex` |
| 4 | `ch:attention_transformers` | `Chapters/Chapter4.tex` |
| 5 | `ch:self_supervised_learning` | `Chapters/Chapter5.tex` |
| 6 | `ch:detection_segmentation` | `Chapters/Chapter6.tex` |

## Rules

- A deck may be split across chapters only if the split is recorded here.
- A deck marked "ignored" must not be used to justify adding tool-specific content to a theory chapter.
- When a new chapter is created, add its row here before writing the chapter.
- If a deck is renamed, update this table and the decision log in the same commit.

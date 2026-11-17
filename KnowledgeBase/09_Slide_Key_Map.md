# Slide-Key Concept Map

This is the inverse of `08_Concept_Map.md`: the **professor's slides are the key**, and each row says where that slide group is covered in the book.

Page numbers are **PDF pages of the deck**, not the printed slide numbers at the bottom of the slides. Consecutive slides that develop one concept are grouped.

## Summary

| Deck | Book chapter | PDF pages | Core coverage | Main gaps |
|---|---|---|---|---|
| `02_AMLCV_neural_networks.pdf` | Chapter 1 | 37 | ~95% | Modular API/code walkthrough (not core). |
| `05_AMLCV_TrainingNN.pdf` | Chapters 1--2 | 96 | ~95% | None in the core; data augmentation and transfer learning are in Chapter 2. |
| `03_AMLCV_convnets.pdf` | Chapter 2 | 32 | ~95% | History/human-brain slides (not core); "enabling progress" is compressed. |
| `06_AML_Sequence_Models_I.pdf` | Chapter 3 | 84 | ~100% | None in the technical core. |
| `07_AML_Sequence_Models_II.pdf` | Chapter 4 | 102 | ~100% | Image captioning with Transformers and BERT conclusions are compressed. |
| `08_AML_Detection_Segmentation.pdf` | Chapter 6 | 148 | ~100% | History, open-source-framework, and repeated outline slides are intentionally skipped. |
| `09_AML_SSL.pdf` | Chapter 5 | 122 | ~95% (estimated) | No core gaps; some ablation/result slides are compressed. |

---

## Deck 02 — Neural Networks (Chapter 1)

| Slides | Lecture content | Book location | Status |
|---|---|---|---|
| 1--5 | Machine learning, computer vision, digital images, image classification | 1.1--1.2 | Complete |
| 6--8 | Linear classifier, Softmax classifier | 1.2.1--1.2.3 | Complete |
| 9 | Regularization | 1.7 | Complete |
| 10 | Stochastic Gradient Descent | 1.6 | Complete |
| 11--26 | Computational graph, simple backprop example, local gradients | 1.3 + FDS exercise | Complete |
| 27--29 | Backprop implementation, gradient patterns, modularized API | 1.3 Notebox + FDS exercise | Partial: the API/code details are not core. |
| 30--33 | Backprop with vectors and matrices | 1.3 + FDS exercise | Complete |
| 34 | Deeper networks | 1.3.1 | Complete |
| 35 | ReLU as the default activation | 1.4.1 | Complete |
| 36 | Full 2-layer implementation in ~20 lines | 1.3 | Partial / not core |
| 37 | Thank you | — | — |

---

## Deck 05 — Training Neural Networks (Chapters 1--2)

| Slides | Lecture content | Book location | Status |
|---|---|---|---|
| 1--2 | Components of CNNs, training overview | 1.1 / 2.3 | Complete |
| 3--20 | Activation functions: Sigmoid, Tanh, ReLU, Leaky ReLU, ELU, GELU | 1.4 | Complete |
| 21--24 | Data preprocessing | 1.9.1 | Complete |
| 25--34 | Weight initialization: constant init, Xavier, Kaiming/He | 1.5 | Complete |
| 35--45 | Batch Normalization, test-time statistics, BN for ConvNets | 1.8.1 | Complete |
| 46--50 | Layer, Instance, Group Normalization and comparison | 1.8.2 | Complete |
| 51--54 | Training vs test error, early stopping | 1.9.2 | Complete |
| 55--70 | Regularization: L1/L2, Dropout, inverted dropout, common pattern | 1.7 | Complete |
| 71--80 | Data augmentation, Cutout, Mixup | 2.9 | Moved to Chapter 2 |
| 81--85 | Choosing hyperparameters | 1.9.3 | Complete |
| 86--96 | Transfer learning and model zoos | 2.10 | Moved to Chapter 2 |

---

## Deck 03 — Convolutional Networks (Chapter 2)

| Slides | Lecture content | Book location | Status |
|---|---|---|---|
| 1--7 | Fully connected vs locally connected vs convolutional net, parameter sharing | 2.2 | Complete |
| 8 | 2D convolution | 2.3 | Complete |
| 9 | Linear systems and superposition | 2.3.2 | Complete |
| 10--12 | Convolution layer, filters, activation maps, multiple channels | 2.3 | Complete |
| 13--15 | History of CNNs, human brain, LeNet characteristics | 2.7 | Partial: historical context, not core. |
| 16--17 | Pooling layer, max pooling | 2.6 | Complete |
| 18--20 | AlexNet, enabling progress in DNNs | 2.7 | Complete; "enabling progress" is compressed. |
| 21--27 | ConvNet as a sequence of layers, numerical examples | 2.3 / 2.5 / 2.6 | Complete |
| 28--29 | Receptive fields | 2.3.4 | Complete |
| 30 | Large ConvNets for image classification | 2.7 | Complete |
| 31--32 | Additional reading, thank you | — | — |

---

## Deck 06 — Sequence Models I (Chapter 3)

| Slides | Lecture content | Book location | Status |
|---|---|---|---|
| 1--15 | Sequence tasks, one-to-many/many-to-one/many-to-many, forecasting | 3.1 | Complete |
| 16--17 | Outline | — | — |
| 18--26 | Temporal Convolutional Networks, causal and dilated convolutions, trade-offs | 3.2 | Complete |
| 27 | Outline | — | — |
| 28--44 | RNN, hidden state, unrolling, many-to-many | 3.3.1--3.3.4 | Complete |
| 45--55 | Sequence-to-sequence examples, character-level language model | 3.3.4--3.3.5 | Complete |
| 56--69 | Image captioning with CNN + RNN | 3.3.6 | Complete |
| 70 | Multilayer/stacked RNNs | 3.3.7 | Complete |
| 71--74 | Vanilla RNN gradient flow | 3.4.1--3.4.2 | Complete |
| 75 | RNN trade-offs | 3.4.3 | Complete |
| 76--82 | LSTM: cell state, gates, gradient highway | 3.5 | Complete |
| 83 | Summary; LSTM and GRU as gated architectures | 3.5.5 / 3.6 | Complete |
| 84 | Thank you | — | — |

---

## Deck 07 — Sequence Models II (Chapter 4)

| Slides | Lecture content | Book location | Status |
|---|---|---|---|
| 1--4 | Title and outline | — | — |
| 5--27 | Seq2seq with RNNs and attention, alignment, context vector | 4.2.1--4.2.4 | Complete |
| 28--38 | Image captioning with RNNs and attention | 4.2.5 | Complete |
| 39--45 | Self-attention, maximum path length, why self-attention | 4.3 | Complete |
| 46 | Outline | — | — |
| 47--54 | Positional encoding: desiderata, sinusoidal and learned | 4.4.1--4.4.2 | Complete |
| 55--59 | Transformer, masked self-attention, general vs self-attention, multi-head | 4.4.4--4.4.5 / 4.5 | Complete |
| 60 | Outline | — | — |
| 61--71 | Transformer networks, image captioning, RNN vs Transformer | 4.5 | Complete; image captioning is compressed. |
| 72 | Outline | — | — |
| 73--81 | Self-similarity, non-local means, Image Transformer | 4.6.1--4.6.3 | Complete |
| 82--83 | Self-attention with relative positional encoding | 4.4.3 | Complete |
| 84--88 | Image captioning with Transformers, ViT vs ResNets, ViT | 4.6.2--4.6.4 | Complete; captioning is a short stage. |
| 89 | Outline | — | — |
| 90--97 | BERT, masked LM, fine-tuning, ELECTRA | 4.7.1--4.7.3 | Complete |
| 98--101 | Production services, distillation, conclusions on BERT | 4.7.4 | Complete; conclusions are compressed. |
| 102 | Thank you | — | — |

---

## Deck 08 — Detection and Segmentation (Chapter 6)

| Slides | Lecture content | Book location | Status |
|---|---|---|---|
| 1--5 | Title and outline | — | — |
| 6--9 | Semantic segmentation, things vs stuff | 6.1--6.2 | Complete |
| 10--14 | Sliding-window segmentation and its limits | 6.2.1 | Complete |
| 15--18 | Fully convolutional networks | 6.2.2 | Complete |
| 19--37 | Nearest neighbor, bed of nails, unpooling, max unpooling, transpose convolution, matrix view | 6.2.3 | Complete |
| 38--42 | U-Net and skip connections | 6.2.4 | Complete |
| 43--45 | Segmentation metrics and data collection | 6.2.5 | Complete |
| 46--53 | Single-object detection, classification + localization | 6.3.1 | Complete |
| 54--60 | Multiple objects, IoU, NMS | 6.3.2 | Complete |
| 61--69 | Selective search and R-CNN | 6.3.3 | Complete |
| 70--92 | Fast R-CNN, RoI pooling, RoI align | 6.3.4 | Complete |
| 93--104 | Faster R-CNN, Region Proposal Network, anchors | 6.3.5 | Complete |
| 105--113 | YOLO, SSD, RetinaNet | 6.3.6 | Complete |
| 114--119 | DETR and set prediction | 6.3.7 | Complete |
| 120--129 | Instance segmentation and Mask R-CNN | 6.4 | Complete |
| 130--135 | Open-source frameworks, evaluation, COCO | 6.3.8 / 6.2.5 | Partial: evaluation is covered, frameworks are skipped. |
| 136--147 | Beyond 2D: dense captioning, scene graphs, 3D detection, Mesh R-CNN | 6.5 | Complete, compressed |
| 148 | Thank you | — | — |

## Deck 09 — Self-Supervised Learning (Chapter 5)

| Slides | Lecture content | Book location | Status |
|---|---|---|---|
| 1--7 | Learned representations, transfer learning motivation | 5.1 | Complete |
| 8--15 | SSL pretext/downstream paradigm, evaluation protocols | 5.2 | Complete |
| 16--17 | Outline | — | — |
| 18--23 | Rotation prediction | 5.3.1 | Complete |
| 24--26 | Relative patch location, jigsaw puzzles | 5.3.2 | Complete |
| 27--32 | Inpainting, context encoders | 5.3.3 | Complete |
| 33--50 | Image and video colorization, tracking emergence | 5.3.4 | Complete |
| 51--59 | Masked Autoencoders (MAE), encoder/decoder, reconstruction | 5.4 | Complete |
| 60--64 | Summary of pretext tasks, toward a general pretext task | 5.4--5.5 | Complete |
| 65--74 | Contrastive representation learning, InfoNCE | 5.5 | Complete |
| 75--89 | SimCLR: augmentations, projection head, NT-Xent, batch size | 5.5.3 | Complete |
| 90--96 | MoCo and MoCo v2 | 5.5.4 | Complete |
| 97--104 | BYOL | 5.6.2 | Complete |
| 105--109 | SimSiam | 5.6.3 | Complete |
| 110--116 | DINO, DINOv2, DINOv3: architecture, scaling, Gram anchoring, post-training | 5.6.4--5.6.6 | Complete |
| 117--120 | Summary of contrastive learning and BYOL/SimSiam; chapter recap | 5.7--5.8 | Complete: replaced by the standard recap table. |
| 121--122 | References, thank you | — | — |

---

## Residual gaps inside mapped decks

These are slides inside decks that are already in the book, but whose content is only partially developed or intentionally compressed.

| Deck | Slides | Concept | Status |
|---|---|---|---|
| 02 | 27--29 | Backprop implementation, gradient patterns, modularized API | Partial: the math is covered, the code/API walkthrough is not. |
| 02 | 36 | Full 2-layer implementation in ~20 lines | Not core; intentionally omitted. |
| 03 | 13--15 | History of CNNs, human brain, LeNet characteristics | Partial: historical context only. |
| 03 | 20 | "Enabling progress in DNNs" | Compressed: data/GPU/algorithm enablers are mentioned only in passing. |
| 07 | 61--71 | Image captioning with Transformers | Compressed: covered as one stage of the vision-to-language evolution. |
| 07 | 76 | Self-similarity in music | Not covered; not core for this course. |
| 07 | 98--101 | Conclusions on BERT | Compressed: the production/distillation takeaway is present. |
| 08 | 49, 130 | Impact of deep learning, open-source frameworks | Not core; skipped. |
| 08 | 136--147 | Beyond 2D: dense captioning, scene graphs, 3D detection, Mesh R-CNN | Compressed to a short section. |
| 09 | 58--59 | MAE ablation studies and comparisons | Not developed in detail; the architecture and objective are covered. |
| 09 | 117--120 | Summary slides for contrastive learning and BYOL/SimSiam | Replaced by the standard `Recap: Key Concepts` table. |

## Decks not mapped

| Deck | Reason |
|---|---|
| `01_AMLCV_intro.pdf` | Non-technical course introduction. |
| `04_AMLCV_Pytorch_recap.pdf` | Practical PyTorch tutorial, excluded by decision. |
| `10_AML_HyperbolicLearning.pdf` | Future chapter. |
| `11_AML_GenAI_VAE_GAN.pdf` | Future chapter. |

## Reading the status column

- **Complete** — the concept is explained in the body text with its equation or example.
- **Partial** — the concept is present but compressed, or only mentioned in a caption/bullet.
- **Moved** — the concept is covered in another chapter by editorial decision.
- **Not core** — historical or implementation detail that does not need full coverage.

When a slide group moves, update both this file and `03_Lesson_Map.md`.

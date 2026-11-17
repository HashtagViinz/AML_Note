# Concept Map: Lectures vs Book

This file maps the technical concepts of each lecture deck to the section of the book where they are covered. It is the reference for coverage checks and for deciding what is still missing.

## Legend

| Status | Meaning |
|---|---|
| **Complete** | The concept is stated and explained in the body text, with its equation or example. |
| **Partial** | The concept is mentioned, but the explanation is shorter than the lecture or lacks an equation/example. |
| **Moved** | The concept belongs to another chapter by editorial decision. |
| **Not core** | Historical, administrative, or tool-specific material that does not need full coverage. |
| **Out of scope** | The deck is intentionally excluded from the book. |

---

## Chapter 1 — Foundations of Deep Learning and Optimization

Decks: `02_AMLCV_neural_networks.pdf` + `05_AMLCV_TrainingNN.pdf` (training foundations).

| Lecture concept | Book location | Status |
|---|---|---|
| Image classification, linear classifier, scores | 1.2 | Complete |
| Softmax classifier and cross-entropy | 1.2.3 | Complete |
| MSE and binary cross-entropy | 1.2.1--1.2.2 | Complete |
| Regularization (L1/L2) | 1.7 | Complete |
| Stochastic Gradient Descent | 1.6 | Complete |
| Computational graph and backpropagation | 1.3 + FDS exercise | Complete |
| Local gradients and chain rule | 1.3 + FDS exercise | Complete |
| Backprop with vectors/matrices | 1.3 Notebox + FDS exercise | Partial: no modular API implementation details, but the math is covered. |
| Deeper networks and ReLU | 1.3--1.4 | Complete |
| Activation functions: Sigmoid, Tanh, ReLU, Leaky ReLU, ELU, GELU, Maxout | 1.4 | Complete |
| Data preprocessing (mean subtraction, normalization) | 1.9.1 | Complete |
| Weight initialization: Xavier and Kaiming/He | 1.5 | Complete |
| Batch Normalization and test-time statistics | 1.8.1 | Complete |
| Layer, Instance, Group Normalization | 1.8.2 | Complete |
| Dropout and inverted dropout | 1.7.1 | Complete |
| Training vs test error, early stopping | 1.9.2 | Complete |
| Hyperparameter search | 1.9.3 | Complete |
| Data augmentation, Cutout, Mixup | 2.9 | Moved to Chapter 2 |
| Transfer learning | 2.10 | Moved to Chapter 2 |

**Coverage:** core ~95%, raw ~85%. The only non-core gap is the detailed modular API/code walkthrough.

---

## Chapter 2 — Convolutional Neural Networks and Computer Vision

Deck: `03_AMLCV_convnets.pdf` + the vision-regularization part of `05_AMLCV_TrainingNN.pdf`.

| Lecture concept | Book location | Status |
|---|---|---|
| Digital image as a tensor, pinhole camera, digitization | 2.1 | Complete |
| Linear systems and superposition | 2.3.2 | Complete |
| Convolution layer, filters, feature maps, channels | 2.3 | Complete |
| Padding, stride, filter size | 2.3.1 | Complete |
| Convolution vs cross-correlation and 180-degree flip | 2.3.3 | Complete |
| Receptive field and its growth | 2.3.4 | Complete |
| Classic filters: identity, edge, blur, sharpen | 2.4 | Complete |
| Output shape and parameter counting for 3D volumes | 2.5 | Complete |
| Max pooling and average pooling | 2.6 | Complete |
| LeNet, AlexNet, VGG, ResNet | 2.7 | Complete |
| Hierarchical visualization of learned features | 2.8 | Complete |
| Data augmentation: flips, crops, color, Cutout, Mixup | 2.9 | Complete |
| Transfer learning and model zoos | 2.10 | Complete |
| History of CNNs and the human-brain analogy | 2.7 (brief context) | Not core: only a short historical mention. |
| "Enabling progress in DNNs" (data, GPU, algorithms) | Not developed | Partial: not a core model concept. |

**Coverage:** core ~95%, raw ~75%. The missing items are historical context, not technical concepts.

---

## Chapter 3 — Sequence Models

Deck: `06_AML_Sequence_Models_I.pdf`.

| Lecture concept | Book location | Status |
|---|---|---|
| Sequence tasks and one-to-many/many-to-one/many-to-many | 3.1.1 | Complete |
| Forecasting and trajectory prediction | 3.1.2 | Complete |
| 1D convolutions on sequences | 3.2.1 | Complete |
| Causal convolutions | 3.2.2 | Complete |
| Dilated convolutions and receptive field | 3.2.2 | Complete |
| TCN trade-offs | 3.2.3 | Complete |
| Recurrence principle and hidden state | 3.3.1 | Complete |
| Vanilla RNN equations | 3.3.2 | Complete |
| Unrolling the computational graph | 3.3.3 | Complete |
| Sequence-to-sequence mappings | 3.3.4 | Complete |
| Character-level language modeling | 3.3.5 | Complete |
| Teacher forcing and autoregressive generation | 3.3.5 | Complete |
| Image captioning with CNN + RNN | 3.3.6 | Complete |
| Multilayer/stacked RNNs | 3.3.7 | Complete |
| BPTT and gradient flow | 3.4.1 | Complete |
| Exploding/vanishing gradients and clipping | 3.4.2 | Complete |
| Vanilla RNN trade-offs | 3.4.3 | Complete |
| LSTM dual state, gates, cell-state highway | 3.5 | Complete |
| GRU and LSTM-vs-GRU comparison | 3.5.5 | Complete |

**Coverage:** core ~100%, raw ~90%. The only raw gaps are repeated slide titles and administrative material.

---

## Chapter 4 — Attention Mechanisms and Transformer Networks

Deck: `07_AML_Sequence_Models_II.pdf`.

| Lecture concept | Book location | Status |
|---|---|---|
| Information bottleneck of vanilla Seq2Seq | 4.2.1 | Complete |
| Bahdanau additive attention | 4.2.2 | Complete |
| Step-by-step alignment example | 4.2.3 | Complete |
| Attention matrices and word reordering | 4.2.4 | Complete |
| Spatial attention / Show, Attend and Tell | 4.2.5 | Complete |
| General attention vs self-attention | 4.3.1 | Complete |
| Query, Key, Value formulation | 4.3.2 | Complete |
| Scaled dot-product and `1/sqrt(D_k)` | 4.3.2 | Complete |
| Maximum path length and complexity table | 4.3.3 | Complete |
| Permutation equivariance | 4.4.1 | Complete |
| Absolute positional encodings | 4.4.2 | Complete |
| Relative positional encodings | 4.4.3 | Complete |
| Causal masking | 4.4.4 | Complete |
| Multi-head self-attention | 4.4.5 | Complete |
| Transformer encoder block | 4.5.1 | Complete |
| Transformer decoder and cross-attention | 4.5.2 | Complete |
| RNN vs Transformer comparison | 4.5.3 | Complete |
| Visual self-similarity and non-local means | 4.6.1 | Complete |
| Vision-to-language pipeline evolution | 4.6.2 | Complete |
| Image Transformer and local self-attention | 4.6.3 | Complete |
| Vision Transformer (ViT) | 4.6.4 | Complete |
| BERT, MLM, NSP, fine-tuning | 4.7.2 | Complete |
| ELECTRA and replaced-token detection | 4.7.3 | Complete |
| Knowledge distillation | 4.7.4 | Complete |
| Image captioning with Transformers | 4.6.2 (one bullet) | Partial: covered as a stage of the evolution, not as a full architecture walkthrough. |
| Conclusions on BERT | 4.7.4 (final paragraph) | Partial: the practical takeaway is present, the slide's broader conclusions are compressed. |
| Self-similarity in music | Not covered | Not core for this course. |

**Coverage:** core ~100%, raw ~90%. The two partial items are synthesis material, not new mechanisms.

---

## Chapter 5 — Self-Supervised Learning

Deck: `09_AML_SSL.pdf`.

| Lecture concept | Book location | Status |
|---|---|---|
| Supervised bottleneck and learned representations | 5.1 | Complete |
| Pretext task / downstream task paradigm | 5.2.1 | Complete |
| Evaluation protocols (linear probe, fine-tuning, semi-supervised) | 5.2.2 | Complete |
| Rotation prediction | 5.3.1 | Complete |
| Relative patch location and jigsaw puzzles | 5.3.2 | Complete |
| Context encoders and inpainting | 5.3.3 | Complete |
| Image and video colorization | 5.3.4 | Complete |
| Masked Autoencoders (MAE) | 5.4 | Complete |
| Linear probing vs fine-tuning for MAE | 5.4.4 | Complete |
| Contrastive learning and InfoNCE | 5.5 | Complete |
| SimCLR | 5.5.3 | Complete |
| MoCo and MoCo v2 | 5.5.4 | Complete |
| BYOL | 5.6.2 | Complete |
| SimSiam | 5.6.3 | Complete |
| DINO | 5.6.4 | Complete |
| DINOv2 | 5.6.5 | Complete |
| DINOv3: scaling, Gram anchoring, post-training | 5.6.6 | Complete |
| Recap of key concepts | 5.8 | Complete: standard table + one-sentence `InsightBox`. |

**Coverage:** core ~95%, raw ~85%. No core gaps identified; the remaining raw gaps are ablation and result slides that are compressed.

---

## Chapter 6 — Object Detection and Segmentation

Deck: `08_AML_Detection_Segmentation.pdf`.

| Lecture concept | Book location | Status |
|---|---|---|
| Task taxonomy: classification, semantic segmentation, detection, instance segmentation | 6.1 | Complete |
| Things vs stuff | 6.1 | Complete |
| Sliding-window segmentation and its limits | 6.2.1 | Complete |
| Fully convolutional networks | 6.2.2 | Complete |
| Nearest neighbor, bed of nails, unpooling, max unpooling, transpose convolution | 6.2.3 | Complete |
| U-Net and skip connections | 6.2.4 | Complete |
| Segmentation metrics (pixel accuracy, IoU, per-class accuracy) | 6.2.5 | Complete |
| Annotation challenges and datasets | 6.2.5 | Complete |
| Single-object detection and multi-task loss | 6.3.1 | Complete |
| Multiple objects, IoU, NMS | 6.3.2 | Complete |
| Selective search and R-CNN | 6.3.3 | Complete |
| Fast R-CNN, RoI pooling, RoI align | 6.3.4 | Complete |
| Faster R-CNN, RPN, anchors | 6.3.5 | Complete |
| YOLO, SSD, RetinaNet | 6.3.6 | Complete |
| DETR and set prediction | 6.3.7 | Complete |
| mAP evaluation | 6.3.8 | Complete |
| Mask R-CNN | 6.4 | Complete |
| Beyond 2D: dense captioning, scene graphs, 3D detection, Mesh R-CNN | 6.5 | Complete, compressed |
| Recap of key concepts | 6.6 | Complete |

**Coverage:** core ~100%, raw ~85%. Historical, open-source-framework, and repeated outline slides are intentionally skipped.

## Decks not in the book

| Deck | Reason | Status |
|---|---|---|
| `01_AMLCV_intro.pdf` | Course introduction, non-technical | Out of scope |
| `04_AMLCV_Pytorch_recap.pdf` | PyTorch tool tutorial | Out of scope by decision |
| `10_AML_HyperbolicLearning.pdf` | Hyperbolic learning | Future chapter |
| `11_AML_GenAI_VAE_GAN.pdf` | Generative AI: VAE and GAN | Future chapter |

## How to update this map

1. Add a row when a new concept is inserted in a chapter.
2. Change `Partial` to `Complete` only when the concept is explained in the body text, not just mentioned in a caption.
3. If a concept moves to another chapter, update both rows and `03_Lesson_Map.md`.
4. Recompute the coverage estimates with the procedure in `04_Coverage_Methodology.md`.

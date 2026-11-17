# Old Exam Question Map

## Source and caveats

`Old_Exam_Question.txt` collects topics reported by students from last year's oral exams. It is **not** an official syllabus: the messages are informal, some topics may belong to the previous year's program, and the sample is small. It is still the best available signal for exam preparation.

The frequency column is therefore approximate. It counts how often a topic appears across the reported exam sessions, not a precise statistical frequency.

## Priority map

| Priority | Topic | Approx. mentions | Book status | Where |
|---|---|---|---|---|
| **Very high** | Attention and Transformers: strengths, inductive bias, complexity, parallelization, scaling factor, RNN comparison | 5+ sessions | Covered | Chapters 4, 5 |
| **Very high** | Self-supervised learning: pretext tasks, SimCLR, MoCo/MoCo v2, BYOL, MAE, DINO, InfoNCE | 8+ sessions | Covered | Chapter 5 |
| **Very high** | Detection and segmentation: Faster/Fast R-CNN, Mask R-CNN, ROI pooling, single-stage detectors, U-Net, transpose convolution | 6+ sessions | Covered | Chapter 6 |
| **High** | Autoencoders vs VAE, VAE structure, autoencoder trivial solution and bottleneck | 5+ sessions | **Missing** | Future generative chapter (deck 11) |
| **High** | GCN/GAT formula, graph attention, oversmoothing | 5+ sessions | **Missing** | Future graph-learning supplement |
| **High** | Hyperbolic geometry: Poincaré model, radius interpretation, exp/log maps, Euclidean-to-hyperbolic | 5+ sessions | **Missing** | Future hyperbolic chapter (deck 10) |
| **Medium-high** | CLIP: training, positives, zero-shot classification | 4 sessions | **Missing** | Future multimodal/CLIP supplement |
| **Medium** | Diffusion models | 3 sessions | **Missing** | Future generative chapter (deck 11) |
| **Medium** | BERT: masking, embeddings, classification/fine-tuning | 2 sessions | Covered / partial | Chapter 4 |
| **Medium** | RNN inductive bias; RNN vs Transformer comparison | 3 sessions | Covered | Chapters 3--4 |
| **Medium** | TCN | 1 session | Covered | Chapter 3 |
| **Medium** | Semantic segmentation and U-Net | 2 sessions | Covered | Chapter 6 |
| **Medium** | Transpose convolution and upsampling | 2 sessions | Covered | Chapter 6 |
| **Medium** | InfoNCE and batch-size dependence | 1--2 sessions | Covered | Chapter 5 |
| **Low-medium** | GANs | 1 session | **Missing** | Future generative chapter (deck 11) |
| **Low-medium** | Hierarchical classification | 2 sessions | **Missing** | Not yet assigned |
| **Low-medium** | Zero-shot learning | 2 sessions | **Missing** | CLIP supplement |
| **Low-medium** | Overmoothing | 3 sessions | **Missing** | Graph/hyperbolic chapter |

## Chapter-by-chapter exam focus

### Chapter 1 — Foundations
Exam-relevant core: backpropagation, activation functions, initialization, normalization, dropout, SGD. These are prerequisites for every other topic; they are rarely the opening question but are often used to check whether the candidate understands the rest.

### Chapter 2 — CNNs
Exam-relevant core: convolution, padding/stride, receptive field, pooling, ResNet, transfer learning. Transpose convolution is examined with segmentation and is covered in Chapter 6.

### Chapter 3 — Sequence models
Exam-relevant core: TCN, RNN, LSTM/GRU, BPTT, gradient clipping. A frequent follow-up is the comparison with Transformers, which is in Chapter 4.

### Chapter 4 — Attention and Transformers
The highest-yield chapter. Frequent questions:
- strengths of attention;
- inductive bias of Transformers;
- computational complexity per layer and maximum path length;
- whether self-attention is parallelizable;
- role of the scaling factor `1/sqrt(D_k)`;
- BERT masking, embeddings, classification/fine-tuning;
- RNN vs Transformer.

### Chapter 5 — Self-supervised learning
The second highest-yield chapter. Frequent questions:
- what a pretext task is and examples;
- SimCLR architecture and NT-Xent;
- MoCo/MoCo v2 queue and momentum encoder;
- BYOL and why it does not collapse;
- MAE masking and asymmetric encoder-decoder;
- DINO, DINOv2, DINOv3;
- InfoNCE and why it depends on the batch/negative set.

### Chapter 6 — Detection and segmentation
The third highest-yield chapter. Frequent questions:
- Fast R-CNN vs Faster R-CNN;
- the losses used by Faster R-CNN;
- single-stage detectors;
- ROI pooling and RoI Align;
- Mask R-CNN architecture;
- semantic segmentation and U-Net;
- transpose convolution and upsampling.

## What the book already does well

- **Attention/Transformers:** complete and detailed; includes the scaling factor, complexity, masking, MHSA, ViT, BERT, ELECTRA, and distillation.
- **SSL:** complete for the methods actually taught this year; DINOv2/v3 are now covered.
- **Detection/segmentation:** complete for the core of deck 08, including Faster R-CNN losses and Mask R-CNN.
- **Sequence models:** TCN, RNN, LSTM, GRU, BPTT are covered.

## What is still missing for a fully exam-proof book

1. **Autoencoders and VAE** — trivial solution, bottleneck, reconstruction vs variational objective, VAE structure.
2. **Graph learning** — GCN formula, graph attention, oversmoothing.
3. **Hyperbolic learning** — Poincaré ball, radius, exp/log maps, hierarchical embeddings.
4. **CLIP and zero-shot classification** — contrastive image-text training and inference.
5. **Diffusion models** — forward/reverse process and sampling.
6. **GANs** — generator/discriminator objective and training.
7. **Hierarchical classification** — definition and use of hyperbolic embeddings.

Items 1, 5, and 6 belong to deck 11 (GenAI). Item 3 belongs to deck 10. Items 2 and 4 are not in the current deck sequence and need a dedicated supplement if the exam keeps asking them.

## Verdict

The book is **strong for attention, SSL, detection/segmentation, and sequence models**. It is **not yet sufficient alone** for the full set of reported oral-exam questions, because generative models, graph learning, hyperbolic learning, and CLIP are missing.

For the next study phase, the highest-value additions are:

1. a **Generative Models** chapter (AE, VAE, GAN, diffusion);
2. a **Hyperbolic Learning** chapter;
3. a short **Graph Neural Networks / oversmoothing** supplement;
4. a short **CLIP / zero-shot** supplement.

## How to update this map

- Add a row when a missing topic is written into a chapter.
- Change `Missing` to `Covered` only when the chapter explains the concept, not when it merely cites it.
- Keep the frequency approximate and based on the collected messages.
- Update `08_Concept_Map.md` and `09_Slide_Key_Map.md` when a topic moves from missing to covered.

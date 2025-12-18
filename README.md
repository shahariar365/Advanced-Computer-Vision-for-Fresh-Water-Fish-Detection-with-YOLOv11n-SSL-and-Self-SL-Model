# Advanced-Computer-Vision-for-Fresh-Water-Fish-Detection-with-YOLOv11n-SSL-and-Self-SL-Model
A computer vision project comparing supervised, semi-supervised (Pseudo-Labeling), and self-supervised (MoCo, SimCLR) learning paradigms using YOLO(v10n, v11n, v12n) models for real-world fish detection. This repository contains the complete work that investigates and compares various deep learning paradigms for automated fish detection. The project consolidates two comprehensive part, moving from a fully supervised baseline to advanced, label-efficient techniques like Semi-Supervised and Self-Supervised Learning.

---

## 🎯 Project Objective

The primary goal of this study was to address the "data-labeling bottleneck" in real-world computer vision applications. We aimed to answer a critical question: **Can we leverage large amounts of unlabeled data to improve or match the performance of a detector trained on a full, manually-labeled dataset?**

To answer this, we used the challenging **SylFishBD dataset**, a collection of real-world images of freshwater fish from market environments in the region of Sylhet, Bangladesh.

## 📂 Repository Contents

This repository is organized into two main parts:

*   ### [**Part 1: Supervised Baseline Comparison**](./Assignment-1/)
    *   This experiment establishes a strong performance baseline by training and evaluating three state-of-the-art, fully supervised models: **YOLOv10, YOLOv11, and YOLOv12**.
    *   **Outcome:** The YOLOv11 model was identified as the best performer, achieving an mAP of **87.53%** and serving as the benchmark for the next phase.

*   ### [**Part 2: Label-Efficient Learning Experiments**](./Assignment-2/)
    *   This experiment simulates a real-world, low-data scenario by partitioning the training set into **20% labeled** and **80% unlabeled** data.
    *   It implements and compares three advanced techniques against the baseline:
        1.  **Semi-Supervised Learning (SSL):** Using the **Pseudo-Labeling** method.
        2.  **Self-Supervised Learning (Self-SL):** Pre-training backbones on the unlabeled data using **Momentum Contrast (MoCo)**.
        3.  **Self-Supervised Learning (Self-SL):** Pre-training backbones on the unlabeled data using **SimCLR**.

---

## 📈 Key Findings & Conclusion

Our experiments yielded a clear and compelling conclusion:

1.  **SSL Surpasses the Baseline:** The **Pseudo-Labeling (SSL)** model achieved an mAP of **88.12%**, successfully improving upon the fully supervised baseline. This proves that a strong model can be enhanced by learning from its own confident predictions on unlabeled data.

2.  **Self-SL is Highly Data-Efficient:** The Self-SL models, despite being fine-tuned on only **20%** of the labeled data, achieved a remarkable mAP of **~86%**. This demonstrates the immense power of self-supervised pre-training to create a powerful feature backbone that can learn a complex task from a very small number of labeled examples.

This project confirms that both SSL and Self-SL are highly effective strategies for building robust, data-efficient object detectors in specialized domains, providing a practical solution to the challenges of data scarcity in real-world machine learning projects.

---

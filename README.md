# Skin Cancer Detection (Melanoma Classification)

## Authors
- **Vinyas Naidu Karri** - [karri.vi@northeastern.edu](mailto:karri.vi@northeastern.edu)
- **Sri Sai Tarun Vemu** - [vemu.s@northeastern.edu](mailto:vemu.s@northeastern.edu)
- **Sathvik Ramappa** - [ramappa.s@northeastern.edu](mailto:ramappa.s@northeastern.edu)

## Project Overview
This project explores the application of **Deep Learning** in detecting melanoma (a dangerous form of skin cancer) using dermoscopic images. We utilized **Convolutional Neural Networks (CNNs)** and transfer learning techniques with architectures like **EfficientNet** and **DenseNet** to achieve high accuracy in distinguishing benign and malignant lesions.

---

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Methodology](#methodology)
4. [Results](#results)
5. [Challenges and Future Work](#challenges-and-future-work)
6. [How to Use](#how-to-use)
7. [References](#references)

---

## Introduction
Skin cancer, particularly melanoma, poses a significant health risk. Early and accurate detection can greatly improve patient outcomes. This project leverages **deep learning** to automate and enhance the diagnostic process, reducing reliance on subjective human analysis.

---

## Dataset
- **Source**: ISIC Archive
- **Details**: 33,126 dermoscopic images of skin lesions from diverse demographics and institutions.
- **Challenges**: Class imbalance (benign cases far outnumber malignant ones).

---

## Methodology
### Data Preprocessing
- Image resizing and normalization.
- Data augmentation (flipping, rotation, zooming) to address class imbalance and improve generalization.

### Models
1. **Baseline CNN**:
   - A simple CNN model for initial benchmarking.
2. **EfficientNetB0 and DenseNet121**:
   - Transfer learning with fine-tuning for improved performance and reduced training time.

### Training
- **Optimizer**: Adam
- **Loss Function**: Sparse Categorical Cross-Entropy
- **Regularization**: Dropout, early stopping

### Metrics
- Accuracy, precision, recall, sensitivity, specificity.

---

## Results
- **Baseline CNN**: Reasonable accuracy but struggled with generalization.
- **EfficientNetB0**: Significant improvement in performance.
- **DenseNet121**: Outperformed all other models, achieving the best balance between sensitivity and specificity.

---

## Challenges and Future Work
### Challenges
- Veru high class imbalance in the dataset led to a bias toward benign cases.

### Future Directions
- Explore synthetic data generation (e.g., GANs) and cost-sensitive learning.
- Incorporate attention mechanisms like Vision Transformers.
- Focus on explainability using Grad-CAM or SHAP for clinical adoption.

---

## How to Use
1. **Clone the Repository**:
    ```bash
    git clone https://github.com/your-username/skin-cancer-detection.git
    ```
2. **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```
3. **Run Training**:
    ```bash
    python train_model.py
    ```
4. **Evaluate the Model**:
    ```bash
    python evaluate_model.py
    ```

---

## References
- [ISIC Archive 2020 Challenge](https://challenge2020.isic-archive.com/)
- [DenseNet121 Architecture](https://www.researchgate.net/figure/DenseNet121-architecture_fig1_363850803)
- [EfficientNetB0 Model](https://www.researchgate.net/figure/EfficientnetB0-Model-Architecture_fig2_378395574)

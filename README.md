# Skin Cancer Classification Using Hybrid Deep Learning and Metadata

## 📌 Project Overview

This project focuses on **Skin Lesion Classification** using the **HAM10000 (Human Against Machine with 10000 training images)** dataset.

The project investigates a **Hybrid Deep Learning approach** that combines image features extracted from a CNN-based architecture with patient metadata to improve skin lesion classification performance.

In addition to model training and evaluation, the project includes **Exploratory Data Analysis (EDA), Explainable AI, Ablation Study, and statistical evaluation** to provide a more comprehensive assessment of the proposed approach.

---

## 📊 Dataset

**HAM10000 Dataset**

The dataset contains **10,015 dermatoscopic images** of pigmented skin lesions categorized into seven diagnostic classes.

### Main Classes

* Melanocytic nevi (nv)
* Melanoma (mel)
* Benign keratosis-like lesions (bkl)
* Basal cell carcinoma (bcc)
* Actinic keratoses (akiec)
* Vascular lesions (vasc)
* Dermatofibroma (df)

### Metadata

The project also utilizes available patient metadata, including:

* Age
* Sex
* Lesion localization
* Other clinical information available in the dataset

---

## 🔍 Exploratory Data Analysis

A detailed **EDA** was performed to understand the dataset and identify potential challenges before model development.

The analysis included:

* Class distribution
* Patient age distribution
* Gender distribution
* Lesion localization
* Relationship between metadata and diagnostic classes
* Image distribution across different lesion categories
* Identification of class imbalance

---

## 🧠 Proposed Hybrid Model

The proposed approach combines **image-based deep learning features** with **patient metadata**.

### Architecture

**Image Branch**

* DenseNet
* Inception

The image features extracted from the deep learning models are combined with metadata features.

### Metadata Branch

Clinical metadata is processed separately and transformed into numerical features suitable for integration with the image representation.

### Feature Fusion

The image representation and metadata representation are combined through a fusion layer before the final classification stage.

```text
             Skin Lesion Image
                    │
          ┌─────────┴─────────┐
          │                   │
      DenseNet            Inception
          │                   │
          └─────────┬─────────┘
                    │
             Image Features
                    │
                    ├──────────────┐
                    │              │
                    │        Metadata Features
                    │              │
                    └──────┬───────┘
                           │
                     Feature Fusion
                           │
                    Classification
                           │
                     Skin Lesion
                       Classes
```

---

## 🧪 Experiments and Evaluation

The project includes several experiments to evaluate the effectiveness and reliability of the proposed approach.

### 1. Confusion Matrix

A confusion matrix was used to analyze:

* True Positives
* True Negatives
* False Positives
* False Negatives
* Per-class classification performance

This provides a detailed view of which lesion classes are being confused by the model.

---

### 2. ROC Curve

Receiver Operating Characteristic (**ROC**) curves were generated to evaluate the classification performance across different decision thresholds.

The analysis includes:

* ROC Curve
* Area Under the Curve (AUC)
* Class discrimination performance

---

### 3. Grad-CAM

**Gradient-weighted Class Activation Mapping (Grad-CAM)** was used to provide visual explanations of the model's predictions.

Grad-CAM highlights the image regions that contributed most to the model's decision.

This helps investigate whether the model is focusing on clinically relevant regions of the skin lesion rather than irrelevant background information.

---

### 4. Ablation Study

An **ablation study** was performed to investigate the contribution of different components of the proposed system.

The study compares different configurations to determine the effect of:

* Image-only features
* Metadata
* Hybrid image + metadata representation
* Different architectural components

This provides evidence for whether the proposed components actually contribute to the final model performance.

---

### 5. McNemar's Test

**McNemar's statistical test** was used to compare the predictions of different classification models.

This test helps determine whether the difference in classification performance between two models is statistically significant rather than simply caused by random variation.

---

## 📈 Evaluation Metrics

The models are evaluated using multiple performance metrics, including:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC
* Confusion Matrix

Statistical analysis is also included to provide a more robust comparison between models.

---

## 🔬 Explainability

Explainability is an important part of the project.

**Grad-CAM** is used to visualize the regions of the input images that contribute to the model's predictions.

This provides additional insight into the model's decision-making process and improves the interpretability of the deep learning system.

---

## 🛠️ Technologies Used

* Python
* PyTorch
* Torchvision
* NumPy
* Pandas
* Scikit-learn
* Matplotlib
* Seaborn
* OpenCV
* PIL
* Grad-CAM
* Statistical Testing

---

## 🎯 Project Objectives

The main objectives of this project are:

1. Develop a deep learning model for skin lesion classification.
2. Investigate the effect of patient metadata on classification performance.
3. Develop a hybrid image + metadata classification approach.
4. Compare different deep learning architectures.
5. Analyze model predictions using Grad-CAM.
6. Perform an ablation study to evaluate individual components.
7. Use statistical testing to compare model performance.
8. Provide a more interpretable and statistically supported evaluation of skin lesion classification.

---

## 🚀 Key Contributions

The project combines several aspects of modern medical AI research:

* **Deep Learning for Medical Image Classification**
* **Metadata-Aware Deep Learning**
* **Hybrid CNN Architecture**
* **Explainable AI using Grad-CAM**
* **Ablation Study**
* **Statistical Model Comparison using McNemar's Test**
* **ROC-AUC Analysis**
* **Comprehensive Model Evaluation**

---

## 📌 Disclaimer

This project is developed for **research and educational purposes**.

The models presented in this repository are **not intended to replace professional medical diagnosis** or clinical decision-making.


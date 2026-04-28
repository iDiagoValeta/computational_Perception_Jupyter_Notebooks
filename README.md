# Computational Perception — Jupyter Notebooks

> Practical lab notebooks for the **Computational Perception** course, part of the Computer Science degree at the [Universitat Politècnica de València (UPV)](https://www.upv.es).

---

## Overview

This repository collects hands-on Jupyter notebooks covering the main topics of the Computational Perception course: classical machine learning, dimensionality reduction, deep learning with Keras, hyperparameter optimisation, and fine-grained image classification. Each notebook (`TL` prefix stands for *Taller*, i.e. workshop) builds on the previous one, progressively introducing more complex techniques.

---

## Notebooks

| # | Notebook | Topics |
|---|----------|--------|
| 02 | [TL02 — PCA](TL02_PCA.ipynb) | Principal Component Analysis, dimensionality reduction, scikit-learn |
| 03 | [TL03 — Generative Linear Models](TL03_GenerativeLinearModels.ipynb) | Naive Bayes, joint distribution modelling, digits dataset |
| 04 | [TL04 — Discriminative Linear Models](TL04_DiscriminativeLinearModels.ipynb) | Logistic Regression, feature engineering, non-linear separability, MNIST |
| 06 | [TL06 — Keras](TL06_Keras.ipynb) | Dense neural networks, ReLU / Softmax, early stopping, dropout |
| 07 | [TL07 — Keras Tuner](TL07_KerasTuner.ipynb) | Hyperparameter tuning, Random Search, optimal architecture for MNIST |
| 08 | [TL08 — KerasHub](TL08_KerasHub.ipynb) | Pretrained models (ResNet, EfficientNet, MobileNet), transfer learning |
| 09 | [TL09 — FGIC](TL09_FGIC.ipynb) | Fine-Grained Image Classification, Oxford 102 Flowers, fine-tuning, data augmentation |

---

## Notebook Descriptions

### TL02 — Principal Component Analysis
Applies PCA to reduce the dimensionality of datasets in machine learning tasks. Uses **scikit-learn** to explore how projecting data onto principal components affects model performance and visualisation.

### TL03 — Generative Linear Models
Introduces generative models that learn the joint distribution P(x, y) of features and class labels. Implements the **Naive Bayes** classifier using the Bayes theorem and evaluates it on the scikit-learn *digits* dataset.

### TL04 — Discriminative Linear Models
Covers discriminative approaches that model P(y|x) directly to learn decision boundaries. Topics include:
- **Logistic Regression** with sigmoid activation
- **Feature engineering** and polynomial transformation to tackle non-linearly separable problems
- Application to the **MNIST** handwritten digit dataset with reduced sample sizes

### TL06 — Introduction to Keras
First contact with the **Keras** deep learning library. Builds fully-connected (dense) neural networks and covers:
- Network architecture: input layer, hidden layers (ReLU), output layer (Softmax)
- Training parameters: epochs, batch size, `validation_split`
- Regularisation techniques: **Early Stopping** and **Dropout**

### TL07 — Keras Tuner
Automates the search for optimal neural network hyperparameters using **Keras Tuner** with Random Search. Finds the best dense architecture for classifying MNIST digits by exploring the number of layers, units per layer, and learning rate.

### TL08 — KerasHub & Transfer Learning
Explores the **KerasHub** official library to load and use pretrained models (ResNet, EfficientNet, MobileNet). Demonstrates how to:
- Load a backbone (`resnet_vd_50_ssld_v2_imagenet`) pretrained on ImageNet
- Use `ImageClassifier` for end-to-end image classification with pretrained weights

### TL09 — Fine-Grained Image Classification (FGIC)
Tackles the challenge of classifying visually similar categories using the **Oxford 102 Flower** dataset (102 classes). Covers:
- Dataset loading with `tensorflow_datasets`
- Transfer learning with ResNet as feature extractor
- **Fine-tuning**: unfreezing upper layers and using a lower learning rate
- **Data augmentation** to improve generalisation
- Training metrics visualisation and final evaluation on the test set

---

## Tech Stack

| Library | Purpose |
|---------|---------|
| `scikit-learn` | Classical ML models, PCA, datasets |
| `numpy` / `matplotlib` | Numerical computing and visualisation |
| `keras` / `tensorflow` | Deep learning framework |
| `keras_tuner` | Hyperparameter optimisation |
| `keras_hub` | Pretrained model hub |
| `tensorflow_datasets` | Standard dataset loading (`Oxford Flowers 102`) |

---

## Requirements

```bash
pip install -r requirements.txt
```

> Python 3.9+ is recommended. GPU support (CUDA) is strongly advised for the Keras notebooks (TL06–TL09).

---

## Course Information

- **Course:** Percepción Computacional (Computational Perception)
- **Degree:** Ingeniería Informática (Computer Science)
- **University:** Universitat Politècnica de València (UPV)
- **Academic Year:** 2024–2025

---

## License

This repository is for academic and educational purposes. No license is explicitly stated; please contact the author before reusing any material.

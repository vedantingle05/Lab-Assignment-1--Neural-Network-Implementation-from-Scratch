# 🧠 Lab Assignment 1 – Neural Network Implementation from Scratch
Neural Network implementation using TensorFlow/Keras on MNIST dataset. Displays weights, gradients, loss and accuracy after every epoch. Test Accuracy: 97.54%


**Student Name:** [Vedant Ingle]
**PRN N0. :** [202402040031]
**Course:** Deep Learning / Artificial Intelligence

---

## 📄 Objective

Implement a simple feedforward neural network using TensorFlow/Keras for multi-class classification on the MNIST dataset. Display all weight values, gradients, loss and accuracy after every epoch.

---

## 📁 Dataset

| Property | Details |
|---|---|
| **Name** | MNIST Handwritten Digits |
| **Official Link** | http://yann.lecun.com/exdb/mnist/ |
| **Kaggle Link** | https://www.kaggle.com/datasets/hojjatk/mnist-dataset |
| **Total Images** | 70,000 |
| **Training Set** | 60,000 images |
| **Test Set** | 10,000 images |
| **Image Size** | 28×28 pixels (grayscale) |
| **Classes** | 10 (digits 0–9) |
| **Auto-download** | ✅ Yes — downloads automatically via TensorFlow |

---

## 🏗️ Model Architecture

```
─────────────────────────────────────────────────
Layer            Neurons    Activation   Params
─────────────────────────────────────────────────
Input Layer       784       —            —
Hidden Layer 1    128       ReLU         100,480
Dropout (0.2)     —         —            0
Hidden Layer 2     64       ReLU         8,256
Dropout (0.2)     —         —            0
Output Layer       10       Softmax      650
─────────────────────────────────────────────────
Total Parameters: 109,386 (427.29 KB)
─────────────────────────────────────────────────
```

---

## ⚙️ Hyperparameters

| Parameter | Value |
|---|---|
| Optimizer | Adam |
| Learning Rate | 0.001 |
| Loss Function | Categorical Cross-Entropy |
| Epochs | 10 |
| Batch Size | 128 |
| Validation Split | 10% |
| Dropout Rate | 0.2 |

---

## 📊 Training Results (Per Epoch)

| Epoch | Train Loss | Train Accuracy | Val Loss | Val Accuracy |
|---|---|---|---|---|
| 1 | 0.474941 | 85.92% | 0.150733 | 95.83% |
| 2 | 0.211265 | 93.85% | 0.111783 | 96.80% |
| 3 | 0.158490 | 95.23% | 0.088470 | 97.50% |
| 4 | 0.128896 | 96.13% | 0.085130 | 97.47% |
| 5 | 0.111847 | 96.56% | 0.078379 | 97.73% |
| 6 | 0.095975 | 97.07% | 0.075383 | 97.80% |
| 7 | 0.084503 | 97.40% | 0.072400 | 97.93% |
| 8 | 0.077054 | 97.61% | 0.071343 | 97.98% |
| 9 | 0.073479 | 97.63% | 0.069018 | 97.88% |
| 10 | 0.064710 | 97.96% | 0.071629 | 98.02% |

---

## ✅ Final Test Results

| Metric | Value |
|---|---|
| **Test Loss** | 0.081967 |
| **Test Accuracy** | **97.54%** |

---

## 📋 What is Displayed Per Epoch

Every epoch prints the following:

- ✅ Training Loss & Accuracy
- ✅ Validation Loss & Accuracy
- ✅ Weight values for every layer (shape, first 5 values, mean, std, min, max)
- ✅ Bias values for every layer
- ✅ Gradient values (mean, std, L2-norm) for every trainable variable

---

## 🎯 Sample Predictions

```
Index   True Label    Predicted    Confidence
─────────────────────────────────────────────
0       7             7            99.99%  ✓
1       2             2            99.97%  ✓
2       1             1            99.99%  ✓
3       0             0            100.00% ✓
4       4             4            99.87%  ✓
5       1             1            100.00% ✓
6       4             4            99.65%  ✓
7       9             9            99.73%  ✓
8       5             5            98.64%  ✓
9       9             9            99.63%  ✓
─────────────────────────────────────────────
Result: 10/10 correct ✅
```

---

## ▶️ How to Run

### Option A — VS Code
```bash
# Step 1: Install Python 3.11
# Download: https://www.python.org/downloads/release/python-3119/

# Step 2: Install dependencies
py -3.11 -m pip install tensorflow numpy matplotlib

# Step 3: Run
py -3.11 neural_network_keras.py
```

### Option B — Google Colab
1. Go to https://colab.research.google.com
2. Upload `neural_network_keras.py`
3. Run — TensorFlow is pre-installed ✅

---

## 📦 Requirements

```
tensorflow>=2.10.0
numpy>=1.23.0
matplotlib>=3.5.0
```

Install all:
```bash
pip install -r requirements.txt
```

---

## 📂 Files in this Repository

| File | Description |
|---|---|
| `neural_network_keras.py` | Main Python code |
| `README.md` | This file |
| `requirements.txt` | Required libraries |

---

## 🔍 Key Observations

1. Loss **decreases** consistently every epoch ✅
2. Accuracy **increases** consistently every epoch ✅
3. Validation accuracy closely follows training accuracy — no overfitting ✅
4. Final test accuracy of **97.54%** achieved in just 10 epochs ✅
5. All 10 sample predictions correct with >98% confidence ✅

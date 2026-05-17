# MNIST & EMNIST CNN Classification

This project implements a **Convolutional Neural Network (CNN)** to classify handwritten **digits and letters** from the MNIST and EMNIST datasets. The model is designed with **no bias terms**, **dropout layers**, and **L2 regularization** to reduce overfitting and achieve more balanced training and validation curves.

---

## Dataset

- **MNIST Digits**: 280,000 grayscale images of handwritten digits (0–9).  
- **EMNIST Digits + Letters**: 383,600 grayscale images of handwritten digits (0–9) and uppercase letters (A–Z).  

**Train/Test split:** 70% training / 30% testing.

---

## Model Architecture

- **Input:** 28x28 grayscale images  
- **Conv2D layer 1:** 8 filters, kernel 5x5, ReLU activation, L2 regularization, **bias enabled**  
- **MaxPooling2D:** pool size 2x2  
- **Dropout:** 10%  
- **Conv2D layer 2:** 16 filters, kernel 5x5, ReLU, L2 regularization, bias enabled  
- **MaxPooling2D:** pool size 2x2  
- **Dropout:** 15%  
- **Flatten**  
- **Dense layer:** 30 units, ReLU, L2 regularization, bias enabled  
- **Dropout:** 20%  
- **Output layer:** 36 units (0–9 digits + A–Z letters), softmax, L2 regularization, bias enabled  

**Optimizer:** Adam, learning rate 0.0003  
**Loss function:** Categorical Crossentropy  
**Metrics:** Accuracy

---

## Features

- Reduced overfitting with **dropout** and **L2 regularization**  
- Balanced training/validation curves  
- Automatic error-based naming of saved model  
- GitHub integration for **automatic commit & push** from Colab  
- Visualizations included:
  - Training & Test **loss curves**
  - Training & Test **accuracy curves**
  - **Confusion matrix** for digits and letters
  - Random correct and incorrect predictions

---

## Usage

1. Clone the repository:

```bash
git clone https://github.com/yoshimabudiman-spec/mnist_cnn_model.git
cd mnist_cnn_model

# MNIST Digit Classification with a Simple Feedforward Neural Network

**Course:** AI / Machine Learning  
**Assignment:** Simple Neural Network (MNIST)  
**Author:** Kyle Kitching 
**Framework Used:** TensorFlow / Keras

---

## Project Overview

This project implements a simple Feedforward Neural Network (FNN) to classify handwritten digits (0–9) from the classic **MNIST** dataset. The goal is to demonstrate foundational deep learning concepts, including data normalization, flattening image inputs, using hidden layers with ReLU activation, and a Softmax output layer for multi-class classification.

---

## Dataset

- **Name:** MNIST Handwritten Digits  
- **Size:** 60,000 training images, 10,000 test images  
- **Image Shape:** 28 x 28 pixels (grayscale)  
- **Number of Classes:** 10 (digits 0–9)

### Pre-processing Steps

1. **Normalization:**  
   - Original pixel values are 0–255.  
   - Scaled to the range **[0, 1]** by dividing by 255.

2. **Flattening:**  
   - Each 28x28 image is reshaped into a **784-dimensional vector**.

3. **Label Encoding:**  
   - Integer labels (0–9) are one-hot encoded into 10-dimensional vectors for use with categorical cross-entropy.

---

## Model Architecture

The model is a fully-connected Feedforward Neural Network with the following layers:

1. **Input Layer**
   - Size: 784 neurons (flattened 28x28 image)

2. **Hidden Layer 1**
   - Type: Dense (Fully Connected)  
   - Neurons: 128  
   - Activation: **ReLU (Rectified Linear Unit)**

3. **Hidden Layer 2**
   - Type: Dense (Fully Connected)  
   - Neurons: 64  
   - Activation: **ReLU**

4. **Output Layer**
   - Type: Dense  
   - Neurons: 10 (one per digit class)  
   - Activation: **Softmax** (outputs class probabilities)

---

## Training Configuration

- **Loss Function:** Categorical Cross-Entropy  
- **Optimizer:** Adam  
- **Metrics:** Accuracy  
- **Batch Size:** 128  
- **Epochs:** 10 (can be adjusted)

Training is performed on the training set, with a portion of the data (e.g., 10%) used for validation.

---

## Results

After training, the model is evaluated on the **test set**.

- **Test Accuracy:** `X.XXXX`  
- **Test Loss:** `Y.YYYY`

> Replace `X.XXXX` and `Y.YYYY` with the actual numbers printed by your notebook.

---

## Files in This Repository

- `mnist_fnn.ipynb` – Jupyter Notebook containing:
  - Data loading
  - Pre-processing (normalization, flattening, label encoding)
  - Model definition and compilation
  - Training loop
  - Evaluation and single-image prediction

- `README.md` – This documentation file.

---

## How to Run

1. Clone or download the repository.
2. Open `mnist_fnn.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab.
3. Install dependencies (if needed):
   ```bash
   pip install tensorflow matplotlib

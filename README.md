# Handwritten Digit Classification using MNIST (Deep Learning)

## Project Description

This project implements a **Multi-Class Classification model** using a Neural Network to recognize handwritten digits (0–9) from the MNIST dataset.

The model is built using **TensorFlow and Keras** and trained on **70,000 grayscale images** of handwritten digits. Each image has a resolution of **28×28 pixels**, which is flattened into a vector of **784 input features**.

The neural network learns to classify each image into one of the **10 digit classes (0–9)**.

---

## Dataset

The project uses the **MNIST dataset** available in Keras.

- Total Images: **70,000**
- Training Images: **60,000**
- Test Images: **10,000**
- Image Size: **28 × 28 pixels**
- Number of Classes: **10 (digits 0–9)**

---

## Model Architecture

The neural network consists of the following layers:

- **Input Layer:** Flatten layer converting 28×28 image into **784 input features**
- **Hidden Layer:** Dense layer with **128 neurons** using **ReLU activation**
- **Output Layer:** Dense layer with **10 neurons** using **Softmax activation**

**Loss Function:** `sparse_categorical_crossentropy`  
**Optimizer:** `Adam`  
**Evaluation Metric:** `Accuracy`

---

## Data Preprocessing

Before training the model, the dataset was prepared using the following steps:

- **Normalization:** Pixel values were scaled from **0–255 to 0–1** by dividing by 255
- **Reshaping:** Images were flattened from **28×28 matrices to 784-dimensional vectors**

These preprocessing steps help improve **training efficiency and model convergence**.

---

## Training

The neural network was trained with the following configuration:

- **Epochs:** 25
- **Validation Split:** 20%

Training and validation accuracy were monitored during training to identify possible **overfitting**.

---

## Results

The trained model achieved approximately **97% accuracy** on the test dataset.

For prediction, the model outputs **10 probability values** representing each digit class.  
The final predicted digit is selected using **`argmax`**, which returns the class with the highest probability.

---

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Google Colab

---

## Project Structure

mnist-digit-classifier
│
├── mnist_digit_classifier.ipynb
├── mnist_model.keras
└── README.md

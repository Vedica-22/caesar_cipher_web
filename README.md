# Automated Caesar Cipher Decoder

This project implements an **Automated Caesar Cipher Decoder** using machine learning. It predicts the Caesar cipher shift used in an encrypted message based on letter frequency analysis and then decrypts the ciphertext into readable English.

---

## Table of Contents

1. [Overview](#overview)
2. [Features](#features)
3. [Dataset](#dataset)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Model Training](#model-training)
7. [Evaluation Metrics](#evaluation-metrics)
8. [Website Interface](#website-interface)

---

## Overview

The **Caesar cipher** is a simple substitution cipher where each letter in the plaintext is shifted a certain number of places down the alphabet.\
This project uses a **Random Forest Classifier** to predict the shift value based on the frequency of letters in the encrypted text, then decrypts the ciphertext accordingly.

---

## Features

- **Letter Frequency Analysis**: Extracts letter distribution from ciphertexts
- **ML-Based Shift Prediction**: Trains a Random Forest Classifier on labeled Caesar cipher data
- **Automatic Decryption**: Uses the predicted shift to convert encrypted text into plaintext
- **Edge Case Handling**: Gracefully deals with low-confidence or anomalous predictions

---

## Dataset

The training dataset is stored in `cipher2.csv` and contains:

| Text  | Shift |
| ----- | ----- |
| "bcd" | 1     |
| "efg" | 2     |
| ...   | ...   |

If you’re using a custom dataset, ensure it follows this same structure:

```csv
Text,Shift
"bcd",1
"efg",2
```

---

## Installation

### Prerequisites

- Python 3.8 or higher
- Install the required Python libraries:

```bash
pip install pandas scikit-learn nltk joblib
```

### Clone the Repository

```bash
git clone https://github.com/yourusername/caesar-cipher-decoder.git
cd caesar-cipher-decoder
```

---

## Usage

### 1. Train the Model

Run the training script to create a model from your dataset:

```bash
python train_model.py
```

This generates a trained model file (e.g., `model.pkl`) using Random Forest.

### 2. Decode a Ciphertext

Use the decoder script to decrypt a ciphertext using the trained model:

```bash
python decode.py
```

---

## Model Training

The model uses a feature vector based on the frequency of each letter (a–z) in the ciphertext.\
A Random Forest Classifier is trained on these features to predict the Caesar shift used.

The trained model is saved using `joblib` and reused during the decoding phase.

---

## Evaluation Metrics

To evaluate model performance, the following metrics are used:

- **Accuracy**: Percentage of correctly predicted shift values
- **Confusion Matrix**: Visualizes prediction errors between true and predicted shifts
- **Sample Decryptions**: Helps verify real-world correctness and intelligibility

---


## Website Interface

![image](https://github.com/user-attachments/assets/b58483d7-0987-4762-97ee-9045e984ada5)

![image](https://github.com/user-attachments/assets/ca85fcaf-d2c6-4134-8205-77c9312a860b)



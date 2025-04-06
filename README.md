# Automated Caesar Cipher Decoder

This project implements an **Automated Caesar Cipher Decoder** using machine learning techniques. The decoder predicts the shift value used in a Caesar cipher by analyzing the frequency of letters in the ciphertext and decrypts it into plaintext.

---

## Table of Contents

1. [Overview](#overview)
2. [Features](#features)
3. [Dataset](#dataset)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Model Training](#model-training)
7. [Evaluation Metrics](#evaluation-metrics)
8. [Contributing](#contributing)
9. [License](#license)

---

## Overview

The Caesar cipher is a substitution cipher where each letter in the plaintext is shifted by a fixed number of positions down the alphabet. This project uses a **Random Forest Classifier** to predict the shift value based on letter frequency analysis of the ciphertext. Once the shift is predicted, the ciphertext is decrypted into readable plaintext.

---

## Features

- **Letter Frequency Analysis**: Computes the frequency of each letter in the ciphertext to predict the shift value.
- **Machine Learning Model**: Uses a Random Forest Classifier for accurate shift prediction.
- **Decryption Logic**: Decrypts ciphertexts using the predicted shift value.
- **Error Handling**: Handles edge cases where predictions may not align with valid English words.

---

## Dataset

The dataset used for training and testing is stored in `cipher2.csv`. It contains:
- `Text`: Ciphertext samples encrypted using various Caesar cipher shifts.
- `Shift`: The corresponding shift values used for encryption.

If you have a custom dataset, ensure it follows the same format:
```csv
Text,Shift
"bcd",1
"efg",2
...

# Automated Caesar Cipher Decoder

This project is a simple Python script that decodes messages encrypted using the Caesar Cipher technique. It uses a brute-force approach to try all 25 possible shifts and displays the results to help identify the correct plaintext message.

## 🔍 What is a Caesar Cipher?

A Caesar Cipher is a type of substitution cipher where each letter in the plaintext is shifted a fixed number of places down the alphabet. It's one of the earliest known encryption techniques, named after Julius Caesar.

## 💡 Features

- Accepts user input (encrypted message)
- Tries all 25 possible shift keys
- Displays all possible decoded outputs
- Helps users manually identify the correct plaintext

## 🧪 Example

Input:
```
WKH HDJOH KDV ODQGHG
```

Output (snippet):
```
Key #1: VJG GCFKG JBU NCPEFC
Key #2: UIF FEBJF IAT MBODEB
Key #3: THE EAGLE HAS LANDED ✅
...
```

## 📜 How to Use

1. Make sure you have Python installed.
2. Run the script:
   ```bash
   python decoder.py
   ```
3. Enter the encrypted message when prompted.
4. Look through the 25 possible outputs and find the readable sentence.

## 📂 Files

- `decoder.py` – The main script that runs the decryption.
- `README.md` – This file.

## 🛠️ Requirements

- Python 3.x
- No external libraries required

## 📌 Note

This script uses brute-force and is intended for educational and beginner cryptography purposes.

## 📖 License

MIT License

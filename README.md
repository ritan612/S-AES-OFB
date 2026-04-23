#  Simplified AES (S-AES) with OFB Mode – Colab Notebook

##  Overview
This notebook implements a **Simplified AES (S-AES)** encryption system and applies it using **Output Feedback (OFB) mode** to encrypt and decrypt files.

It demonstrates core cryptographic concepts including:
- Block cipher design (S-AES)
- Key scheduling
- Encryption & decryption rounds
- File-to-bit conversion
- Stream-like encryption using OFB mode
- Basic **Cryptanalysis techniques** and **Brute Force Attack**
---

##  Features
-  Custom **S-AES implementation**
-  Full **encryption & decryption pipeline**
-  File upload and processing
-  Conversion of files into **bit arrays**
-  Splitting plaintext into **16-bit blocks**
-  Implementation of **OFB (Output Feedback) mode**
-  Demonstration of **brute-force attack**
-  Educational and easy-to-follow structure

---

##  Notebook Structure

### 1. Initialization
- Import required libraries (`numpy`, `random`)
- Setup environment

### 2. Initialization Vector (IV) & Key Input
- Generate or input:
  - Encryption key
  - Initialization Vector (IV)

### 3. File Upload
- Mount Google Drive
- Load file for encryption

### 4. File Processing
- Convert file into a **bit array**
- Prepare data for encryption

### 5. Block Preparation
- Split plaintext into **16-bit blocks**
- Apply padding when necessary

### 6. S-AES Implementation

####  S-Box & Inverse S-Box
- Substitution tables used during encryption/decryption

####  Key Generation
- Functions:
  - `sub_nib()`
  - `rot_nib()`
- Generate round keys

####  Encryption Functions
- `add_round_key`
- `sub_nibbles`
- Shift and mix operations

####  Decryption Functions
- Inverse operations for all encryption steps

### 7. OFB Mode Implementation
- Uses S-AES as a keystream generator

  Steps:
  1. Start with Initialization Vector (IV)
  2. Encrypt IV → generate keystream
  3. XOR keystream with plaintext → ciphertext
  4. Repeat for all blocks

### 8. Cryptanalysis & Security Evaluation

####  Brute-Force Attack
The notebook includes a demonstration of a **brute-force attack** on S-AES:
- Tries all possible keys in the key space
- Attempts to recover the correct key from ciphertext
- Highlights the **small key size weakness** of S-AES

####  Observations
- S-AES uses a **16-bit key**, making it vulnerable to exhaustive search
- Brute-force attacks are **computationally feasible**
- This demonstrates why real-world AES uses **128-bit or larger keys**

####  Educational Purpose
This section helps illustrate:
- How attackers can break weak encryption systems
- The importance of **key size in cryptographic security**
- Fundamental ideas behind **cryptanalysis**

---

##  How to Use

1. Open the notebook in **Google Colab**
2. Run all initialization cells
3. Enter:
   - Encryption key
   - Initialization Vector (IV)
4. Upload your file or mount Google Drive
5. Run encryption cells
6. Run decryption to verify correctness
7. Execute the **brute-force section** to test key recovery

---

##  Concepts Covered
- Symmetric encryption
- Block ciphers
- Stream cipher behavior via OFB
- Bitwise operations
- Cryptographic transformations
- Brute-force attacks
- Basic cryptanalysis


##  Notes
- This is a **simplified educational implementation** of AES
- Not secure for real-world cryptographic use
- Designed for learning and experimentation

---

##  Requirements
- Python 3
- Google Colab environment
- Libraries:
  - `numpy`

---

##  Authors
Rita Nassar and Maya Bouban

---

##  License
This project is for educational purposes.

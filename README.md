#  Simplified AES (S-AES) with OFB Mode – Colab Notebook

##  Overview
This notebook implements a **Simplified AES (S-AES)** encryption system and applies it using **Output Feedback (OFB) mode** to encrypt and decrypt files.

It demonstrates core cryptographic concepts including:
- Block cipher design (S-AES)
- Key scheduling
- Encryption & decryption rounds
- File-to-bit conversion
- Stream-like encryption using OFB mode

---

##  Features
-  Custom **S-AES implementation**
-  Full **encryption & decryption pipeline**
-  File upload and processing
-  Conversion of files into **bit arrays**
-  Splitting plaintext into **16-bit blocks**
-  Implementation of **OFB (Output Feedback) mode**
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



##  How to Use

1. Open the notebook in **Google Colab**
2. Run all initialization cells
3. Enter:
   - Encryption key
   - Initialization Vector (IV)
4. Upload your file or mount Google Drive
5. Run encryption cells
6. Run decryption to verify correctness

##  Concepts Covered
- Symmetric encryption
- Block ciphers
- Stream cipher behavior via OFB
- Bitwise operations
- Cryptographic transformations



##  Notes
- This is a **simplified educational implementation** of AES
- Not secure for real-world cryptographic use
- Designed for learning and experimentation



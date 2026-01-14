# RSA-Based-Encryption-and-Decryption-Across-Multimodal-Data

MATLAB implementation of RSA cryptography across multiple platforms: numbers, text, images, audio, and video. This project explores asymmetric encryption, key generation ($N=p \times q$), and data integrity. Includes advanced simulations on the impact of noise on ciphertext, featuring CRC error detection and Hamming Code error correction.

# Multi-Platform RSA Encryption & Error Correction in MATLAB

This project implements the **RSA (Rivest-Shamir-Adleman)** algorithm to encrypt and decrypt various data types, including numbers, text, images, audio (.WAV), and video. It also explores the impact of noise on ciphertext and implements error detection (CRC) and correction (Hamming Codes).

## 🚀 Features
- **Multi-Format Support:** Handles 1D (text/numbers) and 2D/3D (images/video) data.
- **Signal Processing:** Audio bit-manipulation and binary video reading.
- **Robustness Testing:** Investigation of noise interference in cryptographic channels.
- **Error Control:** Implementation of Cyclic Redundancy Check (CRC) and Hamming (7,4) codes.

## 🛠 How it Works
The system follows the standard RSA mathematical foundation:
1. **Key Generation:** $N = p \times q$
2. **Encryption:** $C = M^e \pmod N$
3. **Decryption:** $M = C^d \pmod N$



[Image of RSA algorithm flowchart]


## 📊 Results
### Image Encryption
To encrypt images, the 2D matrix is flattened into a 1D array, processed, and then reshaped for visualization.



### Noise & Error Correction
We analyzed how noise affects the decryption process and used Hamming codes to recover data integrity.
- **Formula used:** $2^n \geq m + n + 1$

## 📂 Project Structure
- `RSA_Text.m`: Script for text and ASCII conversion.
- `RSA_Image.m`: Script for 1D/2D image transformation.
- `RSA_Multimedia.m`: Audio and Video binary processing.
- `Noise_Analysis.m`: Simulations of signal interference and CRC checks.

## 📝 Discussion & Limitations
- **Constraint:** Message size $M$ must be less than modulus $N$.
- **Security:** Small prime numbers are used for demonstration; 2048-bit primes are recommended for production.
- **Optimization:** For video data, we utilized `fread` for binary efficiency rather than frame-by-frame processing.

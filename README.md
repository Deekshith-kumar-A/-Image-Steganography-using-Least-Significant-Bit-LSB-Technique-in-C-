# 🕵️‍♂️ Image Steganography Using Least Significant Bit (LSB) Technique in C

A **C-based Steganography System** that hides secret data inside BMP image files using **Least Significant Bit (LSB)** encoding.  
This project demonstrates secure data hiding and retrieval using **bitwise operations**, **file handling**, and **data structures** in C.

---

## 🧩 Overview

Steganography is the practice of concealing information within other digital media.  
In this project:
- A **secret text file** is encoded into a **BMP image** without visible distortion.
- The same image can later be **decoded** to retrieve the hidden data.

---

## ⚙️ Features

- 🔐 Encode any text file into a `.bmp` image  
- 🔎 Decode and extract hidden messages accurately  
- 📁 Validate all file formats and handle errors gracefully  
- 🧠 Efficient LSB-based bitwise embedding  
- 🧩 Modular design with separate encoding/decoding logic  
- 💾 Safe handling of BMP headers and pixel data  

---

## 📁 Project Structure

📦 Steganography
┣ 📜 main.c
┣ 📜 encode.c
┣ 📜 decode.c
┣ 📜 encode.h
┣ 📜 decode.h
┣ 📜 types.h
┣ 📜 common.h
┣ 🖼️ beautiful.bmp # Input cover image
┣ 📄 secret.txt # Secret data file
┗ 🖼️ image.bmp # Encoded output image


---

## 🧠 How It Works

### 🔹 Encoding
1. Read source BMP and secret text file  
2. Copy BMP header to a new image  
3. Embed:
   - Magic string (to identify encoded images)  
   - Secret file extension and size  
   - Secret data bits into pixel LSBs  
4. Generate encoded output image  

### 🔹 Decoding
1. Read the encoded BMP  
2. Verify the magic string  
3. Extract:
   - File extension, size, and data bits  
4. Reconstruct the hidden file  

---

## 🖥️ Usage
```bash
🔸 Encode Data

./a.out -e <input_image.bmp> <secret.txt> <output_image.bmp>
🧪 Sample Output
All files opened successfully.
Width = 1024
Height = 768
Image has enough capacity to hold secret data.
BMP Header copied successfully.
Magic string encoded successfully.
Secret file extension encoded successfully.
Secret file encoded successfully.
Encoding completed successfully.

🔸 Decode Data

All files opened successfully.
Magic string found. Image is encoded.
Secret file extension size decoded successfully.
Secret file extension decoded successfully.
Secret file size decoded successfully.
Secret file decoded and written to output file successfully.
Decoding completed successfully.
```
👨‍💻 Author
```
Deekshith Kumar A
🎓 Electronics and Communication Engineering
💼 Passionate about Embedded Systems, Cybersecurity, and Software Development
🔗 https://github.com/Deekshith-kumar-A

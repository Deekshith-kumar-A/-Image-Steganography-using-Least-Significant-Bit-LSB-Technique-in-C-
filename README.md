🕵️‍♂️ Steganography Project in C

A C-based Steganography System that securely hides secret data (like text files) inside image files (.bmp) without altering the visible image.
The project supports both Encoding (hiding data) and Decoding (extracting hidden data) operations using Least Significant Bit (LSB) manipulation.

📁 Project Overview

This project demonstrates the concept of Steganography, where information is concealed within digital media.
In this implementation:

A secret text file is encoded into a BMP image.

The same image can later be decoded to retrieve the hidden message.

It uses bitwise operations, file handling, and data manipulation techniques to perform the process efficiently.

⚙️ Features

✅ Encode a secret text file into a BMP image
✅ Decode the hidden message from an encoded image
✅ Validate input arguments and file formats
✅ Handles BMP headers carefully without distortion
✅ Error handling for missing or invalid files
✅ Modular design with separate encode/decode modules

🧩 Project Structure
📦 Steganography
 ┣ 📜 main.c
 ┣ 📜 encode.c
 ┣ 📜 decode.c
 ┣ 📜 encode.h
 ┣ 📜 decode.h
 ┣ 📜 types.h
 ┣ 📜 common.h
 ┣ 📜 beautiful.bmp        # Sample input image
 ┣ 📜 secret.txt           # Secret data file
 ┗ 📜 image.bmp            # Encoded output image

🧠 How It Works
🔹 Encoding Process:

Read the source BMP image and secret text file.

Copy the BMP header to a new file.

Hide a magic string (like #*) to identify encoded images.

Embed:

Secret file extension size

Secret file extension

Secret file size

Secret file data
— All inside the least significant bits (LSB) of image pixels.

Save the encoded image.

🔹 Decoding Process:

Read the encoded BMP image.

Verify the magic string to confirm it’s encoded.

Extract:

Secret file extension size

Secret file extension

Secret file size

Secret data

Reconstruct the hidden file.

🖥️ Usage
🔸 Encode:
./a.out -e <input_image.bmp> <secret.txt> <output_image.bmp>


Example:

./a.out -e beautiful.bmp secret.txt image.bmp

🔸 Decode:
./a.out -d <encoded_image.bmp> <output_secret.txt>


Example:

./a.out -d image.bmp output.txt

🧪 Sample Output
All files opened successfully.
width = 1024
height = 768
Image has enough capacity to hold secret data.
BMP Header copied successfully.
Magic string encoded successfully.
Secret file extension encoded successfully.
Secret file encoded successfully.
Encoding completed successfully.

🛠️ Technologies Used

Language: C

Concepts: Bitwise Operations, File I/O, Pointers, Structures

Compiler: GCC

Platform: Linux / Windows

🧰 Skills Gained

Strong understanding of file handling in C

Hands-on experience with binary data manipulation

In-depth knowledge of LSB steganography

Implementation of modular programming in C

💡 Future Enhancements

Add password-based encryption before encoding

Support for image formats like PNG or JPG

GUI-based interface for easier use

Integration with cryptography algorithms (AES, RSA)

👨‍💻 Author

Deekshith Kumar A
🎓 Electronics and Communication Engineering
💼 Passionate about Embedded Systems, Security, and Software Development
🔗 GitHub Profile

Steganography Project in C

A C-based Steganography System that securely hides secret data (like text files) inside image files (.bmp) without altering the visible image.
The project supports both Encoding (hiding data) and Decoding (extracting hidden data) operations using Least Significant Bit (LSB) manipulation.

Project Overview

This project demonstrates the concept of Steganography, where information is concealed within digital media.
In this implementation:

A secret text file is encoded into a BMP image.

The same image can later be decoded to retrieve the hidden message.

It uses bitwise operations, file handling, and data manipulation techniques to perform the process efficiently.

⚙️ Features

1. Encode a secret text file into a BMP image
2. Decode the hidden message from an encoded image
3. Validate input arguments and file formats
4. Handles BMP headers carefully without distortion
5. Error handling for missing or invalid files
6. Modular design with separate encode/decode modules

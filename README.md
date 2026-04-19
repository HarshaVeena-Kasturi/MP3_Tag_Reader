# 🎵 MP3 Tag Reader and Editor (C Language)

## 📌 Overview

This project is a command-line based MP3 Tag Reader and Editor developed in the C programming language. It is designed to read and modify **ID3v2 metadata tags** embedded within MP3 files.

The application directly accesses and manipulates binary data in MP3 files without altering the actual audio content, ensuring safe and efficient metadata handling.

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/2e8a58f0-1a8a-40af-86d4-2b6e607320e4" />


## 🎯 Objective

The primary objective of this project is to:

* Understand binary file handling in C
* Work with structured data formats like ID3v2
* Build a real-world file processing application
* Implement modular and reusable code design

---

## ✨ Key Features

### ➤ View MP3 Metadata

* Reads ID3v2 tags from MP3 files
* Displays important fields such as:

  * Title
  * Artist
  * Album
  * Year
  * Genre

---

### ➤ Edit MP3 Metadata

* Allows modification of selected fields
* Updates metadata directly in the file
* Maintains file integrity and audio content

---

### ➤ Safe File Handling

* Works on binary data without corruption
* Ensures only metadata portion is modified
* Preserves original audio stream

---

### ➤ Menu-Driven Interface

* User-friendly CLI menu
* Easy navigation between view and edit operations

---

## ⚙️ Working Principle

1. User provides an MP3 file as input
2. Program reads ID3v2 header
3. Extracts metadata frames (TIT2, TPE1, TALB, etc.)
4. Displays information to the user
5. If editing is selected:

   * User inputs new values
   * Program updates corresponding frames
6. File is rewritten with updated metadata

---

## 🛠️ Technologies Used

* **Programming Language:** C
* **File Handling:** Binary file operations
* **Standard Used:** ID3v2 metadata format
* **Compiler:** GCC
* **Platform:** Linux / Ubuntu

---

## 📂 Project Structure

MP3_Tag_Reader/
│
├── main.c        # Entry point and menu handling
├── view.c        # Reads and displays MP3 metadata
├── edit.c        # Edits metadata fields
├── common.c      # Utility functions
├── mp3.h         # Header definitions and structures
└── README.md     # Documentation

---

## 🚀 How to Run

1. Open terminal in project directory
2. Compile the program:
   ```
   gcc -o mp3tag mp3_main.c mp3_edit.c mp3_view.c functions.c
   ```
3. Display ID3v2 tags from an MP3 file:
   ```
   ./mp3tag -v sample.mp3
   ```
4.  Modify a specific tag (title, artist, etc.) in an MP3:
 ```
  ./mp3tag -e -t "New Title" sample.mp3
   ```
  -t: Title (TIT2),
  
-a: Artist (TPE1),

-A: Album (TALB),

-y: Year (TYER),

-m: Genre/Music (TCON),

-c: Comment (COMM)

5.  Show usage info:
 ```
  ./mp3tag --help
   ```
---
## 💡 Applications

* Music library management systems
* Media player metadata handling
* Embedded audio systems
* Learning binary file processing

---

## ⚠️ Limitations

* Supports only ID3v2 tags
* Limited to basic metadata fields
* CLI-based (no GUI)

---

## 📌 Conclusion

This project demonstrates how low-level file handling in C can be used to build a practical application for managing MP3 metadata. It provides hands-on experience with binary data manipulation and structured file formats.

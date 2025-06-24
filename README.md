# File Manager in C

## Overview
This File Manager is a C-based command-line tool designed for efficiently managing files and directories on Linux-based systems. Developed as an end-semester project for the course **Problem Solving and C Programming**, it provides a user-friendly interface to perform common file operations such as viewing, deleting, renaming, copying, and moving files. Additionally, it supports advanced features like file encryption/decryption, hiding files in images, sorting, and filtering files.

## Features
- **File Operations**: View, delete, rename, copy, and move files.
- **File Manipulation**: Encrypt/decrypt text files and hide files within images.
- **Directory Management**: List files in a directory, create files/folders.
- **Sorting and Filtering**: Sort files alphabetically or by size, and filter using regular expressions.
- **User Interface**: Terminal-based with colored output using ANSI escape codes for better readability.

## Prerequisites
- **Operating System**: Linux-based system (developed and tested on Linux).
- **Compiler**: GCC or any C compiler compatible with C99 or later.
- **Dependencies**: Standard C libraries (`stdio.h`, `stdlib.h`, `string.h`, `dirent.h`, `sys/stat.h`, `regex.h`, `ctype.h`).

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/LostLuinor/File-Manager-C.git
   cd File-Manager-C
   
   ```
2. Compile the source code:
   ```bash
   gcc fileManager.c -o fileManager
   ```
3. Run the program:
   ```bash
   ./fileManager
   ```
   
## Usage
1. Launch the program (`./fileManager`).
2. Enter the working directory when prompted or confirm the current directory.
3. Choose a function by entering the highlighted letter (e.g., `O` for Open, `D` for Delete).
4. Follow the prompts to perform operations like creating files/folders, sorting, or encrypting files.
5. To continue performing operations, enter `y` when prompted; otherwise, exit.

### Example
```bash
$ ./fileManager
Which directory do you want me to work on? /home/user/documents
Your working directory: /home/user/documents
1. cat.jpg
2. fileManager.c
3. document.txt
[I]NFO [O]PEN [R]ENAME [M]OVE [D]ELETE [S]ORTING [F]ILTER FI[N]D [E]NCRYPT [D]ECRYPT [Z]IP CRE[A]TE [U]NZIP [H]IDE 
Just enter the index against the functions: D
Which file: Please enter number shown against files to delete: 1
Deleting...
The file has been successfully deleted.
```
## Key Functions
- `Intro()`: Displays a welcome message for the File Manager with a green-colored title and calls `Functions()` to show available operations.
- `GetDir()`: Reads and stores file names in the specified directory, excluding `"."` and `".."`, up to a maximum of 500 files.
- `WorkingDir()`: Prompts the user to confirm or change the working directory, then loads its contents using `GetDir()`.
- `PickFeature()`: Allows the user to select a file operation by entering a highlighted letter.
- `DelFile()`: Deletes a specified file from the current directory after user confirmation.
- `SearchFile()`: Searches for files in the directory using regular expression pattern matching.
- `SortFiles()`: Sorts files alphabetically or by size based on user preference.
- `FilterFile()`: Filters files based on user-defined criteria using regular expressions.
- `OpenFile(int n)`: Opens the file at index `n` with the system's default application or text editor.
- `RenameFile(int n)`: Renames the file at index `n` using a new name provided by the user.
- `MoveFile(int n)`: Moves the file at index `n` to a user-specified destination directory.
- `FileInfo(int n)`: Displays detailed information such as size and permissions for the file at index `n`.
- `EncryptFile()` / `DecryptFile()`: Encrypts or decrypts text files, limited to those editable by a text editor.
- `ZipFile()`: Compresses a file into a zip archive for storage or transfer.
- `UnzipFile()`: Extracts files from a zip archive in the current directory.
- `HideFile()`: Hides a file by embedding it within an image for added security.
- `FileSize(int n)`: Returns the size of the file at index `n` in bytes.
- `Create()`: Creates new files or folders in the current directory based on user input.
- `ClearScreen()`: Clears the terminal screen using the system's clear command.
- `EnterToContinue()`: Waits for the user to press a key to continue execution.
- `LowerToUpper(char *s)`: Converts a string to uppercase for case-insensitive input handling.
- `ShowFilesInDir()`: Displays a numbered list of files in the current directory for selection.
- `Functions()`: Prints a menu of available file operations with highlighted letters for user selection.

## Limitations
- Cannot access directories above the File Manager’s location.
- Encryption/decryption limited to text files editable by a text editor.
- Cannot decrypt unencrypted files.
- Folder deletion is not supported.

## Future Improvements
- Add password protection for files.
- Enhance the UI to allow navigation using arrow keys and Enter.
- Enable access to all directories, regardless of the program’s location.
- Improve user interface for better usability.

## Testing
The project was tested for key functionalities:
- **Sorting**: Successfully sorts files alphabetically and by size.
- **Deletion**: Successfully deletes files (e.g., `cat.jpg`).
- **Encryption/Decryption**: Creates encrypted files and deletes the original upon decryption.

## References
- [Linux for Devices](https://www.linuxfordevices.com/)
- [JavaTpoint C Tutorial](https://www.javatpoint.com/c-programming-language-tutorial)
- [Stack Overflow](https://stackoverflow.com/)
- [POSIX dirent.h](https://pubs.opengroup.org/onlinepubs/7998799/xsh/dirent.h.html)
- [Code for Win](https://codeforwin.org/c-programming/)

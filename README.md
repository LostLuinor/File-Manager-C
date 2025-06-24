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
   git clone https://github.com/<your-username>/File-Manager-C.git
   cd File-Manager-C
   ```
2. Compile the source code:
   ```bash
   gcc filemgr.c -o filemgr
   ```
3. Run the program:
   ```bash
   ./filemgr
   ```

## Usage
1. Launch the program (`./filemgr`).
2. Enter the working directory when prompted or confirm the current directory.
3. Choose a function by entering the highlighted letter (e.g., `O` for Open, `D` for Delete).
4. Follow the prompts to perform operations like creating files/folders, sorting, or encrypting files.
5. To continue performing operations, enter `y` when prompted; otherwise, exit.

### Example
```bash
$ ./filemgr
Which directory do you want me to work on? /home/user/documents
Your working directory: /home/user/documents
1. cat.jpg
2. filemgr.c
3. document.txt
[R]EN [O]PEN [E]NAME [M]OVE [D]ELETE [S]ORTING [F]ILTER [I]NFO [E]NCRYPT [D]ECRYPT [Z]IP [C]REATE
Just enter the index against the functions: D
Which file: Please enter number shown against files to delete: 1
Deleting...
The file has been successfully deleted.
```
## Key Functions
- `ClearScreen()`: Clears the terminal screen using the `clear` command.
- `GetDir()`: Reads and stores file names in the specified directory.
- `WorkingDir()`: Prompts the user to confirm or change the working directory.
- `SortFiles()`: Sorts files alphabetically or by size.
- `EncryptFile()` / `DecryptFile()`: Encrypts or decrypts text files.
- `Create()`: Creates new files or folders.

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

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

# GoFiler

GoFiler is a file management system built with Go and C++. This utility allows you to create, delete, rename, move files, and much more. It even provides additional utilities for checking file system integrity, managing permissions, and inspecting disk space.

## Table of Contents

1. [Installation](#installation)
2. [Usage](#usage)
3. [Go Codebase](#go-codebase)
4. [C++ Codebase](#c-codebase)
5. [Build](#build)
6. [License](#license)

## Installation

To install the GoFiler system, clone this repository to your local machine:

```bash
git clone https://github.com/Dominic-Wassef/gofiler.git
```

## Usage
For the C++ version:
```bash
./gofiler_cpp [path]
```

For the Go version:
```bash
./gofiler [option] [arguments]
```

## Go Codebase

The Go codebase provides a comprehensive set of file management functionalities. It's equipped with a user-friendly CLI to perform a variety of operations such as creating, deleting, renaming and moving files, as well as reading from and writing to files.

### Files and Directories

- `main.go`: This is the entry point of the Go application. It interprets command-line arguments and dispatches the appropriate file management functions.

- `file_operations.go`: This file provides basic file operations like creation, deletion, renaming and moving of files.

- `file_management.go`: This file contains more complex file management operations including directory management and file search.

- `file_backup.go`: This file holds functions related to backing up files, such as creating and restoring backups.

- `file_compression_encryption.go`: This file includes functions to compress and encrypt files, providing an additional layer of security for sensitive data.

- `file_collaboration.go`: This file is responsible for collaboration features, allowing multiple users to work on the same files.

- `file_metadata.go`: This file deals with file metadata, allowing you to read and modify information like creation date, modification date, and more.

### Commands

The exact list of commands depends on the functions implemented in the respective files. For a basic example:

- Create a new file: `-create="filename"`<br />
Example: `./gofiler -create="myfile.txt"`

- Read a file: `-read="filename"`<br />
Example: `./gofiler -read="myfile.txt"`

- Write to a file: `-write="filename" -data="data to write"`<br />
Example: `./gofiler -write="myfile.txt" -data="Hello, world!"`

- Append to a file: `-append="filename" -data="data to append"`<br />
Example: `./gofiler -append="myfile.txt" -data="This is more data"`

- Delete a file: `-delete="filename"`<br />
Example: `./gofiler -delete="myfile.txt"`

- Rename a file:` -rename="oldname,newname"`<br />
Example: `./gofiler -rename="oldfile.txt,newfile.txt"`

- Move a file: `-move="src,dest"`<br />
Example: `./gofiler -move="path/to/old/location.txt,path/to/new/location.txt"`

- List backups for a file: `-listBackups="filename"`<br />
Example: `./gofiler -listBackups="myfile.txt"`

Remember that these flags should all be preceded by a hyphen (-) and the arguments should be in quotes. Multiple flags can be used at the same time, but some combinations may not make sense (like -read and -write used together).

## C++ Codebase
The C++ codebase provides additional file system utilities like checking file system integrity, managing permissions, and checking disk space.

### Files and Directories
- `file_system_operations.cpp`: Contains the FileSystemOperations class for performing file operations.

- `file_optimization.cpp`: Contains the FileOptimizer class for performing file system operations and checks.

### Main Features<br />
- `CheckFileSystemIntegrity`: Checks the file system integrity.

- `RepairFileSystem`: Repairs the file system.

- `ManagePermissions`: Manages the file permissions.

- `CheckDiskSpace`: Checks the disk space.

## Build
We provide a Makefile for building both the Go and C++ codebases:

To build both:
```bash
make
```

To build the Go codebase:
```bash
make go-build
```

To build the C++ codebase:
```bash
make cpp-build
```

To clean the go build:
```bash
make go-clean
```

To clean the cpp build:
```bash
make cpp-clean
```

## License
[MIT](https://choosealicense.com/licenses/mit/)
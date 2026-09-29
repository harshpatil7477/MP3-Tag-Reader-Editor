# MP3 Tag Reader and Editor

A C-based MP3 Tag Reader and Editor that allows users to view and modify ID3 metadata stored in MP3 files. The project demonstrates binary file handling, command-line arguments, file pointers, structures, and endian conversion.

## Features

* View MP3 metadata
* Edit MP3 metadata
* Supports:

  * Title
  * Artist
  * Album
  * Year
  * Genre
  * Comment
* Uses binary file operations
* Creates a new MP3 file while editing

## Technologies Used

* C Programming
* File Handling
* Command Line Arguments
* ID3 Tags
* Binary File Processing

## Compilation

```bash
gcc main.c view.c edit.c -o mp3reader
```

## Usage

### View MP3 Details

```bash
./mp3reader -v original.mp3
```

### Edit Metadata

```bash
./mp3reader -e -t "New Title" original.mp3
```

```bash
./mp3reader -e -a "New Artist" original.mp3
```

```bash
./mp3reader -e -A "New Album" original.mp3
```

```bash
./mp3reader -e -y "2026" original.mp3
```

## Project Flow

```text
Command Line Arguments
        ↓
   Argument Validation
        ↓
   Open MP3 File
        ↓
 Read ID3 Header / Frames
        ↓
View or Edit Metadata
        ↓
  Generate Output File
```

## ID3 Tags Used

| Tag  | Description |
| ---- | ----------- |
| TIT2 | Title       |
| TPE1 | Artist      |
| TALB | Album       |
| TYER | Year        |
| TCON | Genre       |
| COMM | Comment     |

## Learning Outcomes

* Understanding MP3 ID3 metadata
* Working with binary files using `fread()` and `fwrite()`
* Using `fseek()` for file-pointer movement
* Handling command-line arguments using `argc` and `argv`
* Understanding big-endian and little-endian data
* Implementing modular C programming

## Author

**Harsh Patil**

GitHub: [harshpatil7477](https://github.com/harshpatil7477)

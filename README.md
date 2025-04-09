# 🔍 Inverted Search Project

**Inverted Search** is a file-based search engine implemented in C. It scans multiple input files, builds an inverted index, and allows efficient word-based search queries across the indexed content. The project is structured modularly to support updating, saving, and displaying the database.

---

## 📁 Project Structure

```
Project/
├── Outputs/
│   ├── OUTPUT_MAGE_1.jpg       # Output image file 1
│   └── OUTPUT_MAGE_2.jpg       # Output image file 2
│
├── Source/
│   ├── main_DR.c               # Main DR module source
│   ├── display_DR.c            # Display module source
│   ├── No_wilditions.c         # No wilditions module source
│   ├── main.c                  # Main program source
│   ├── save_DR.c               # Save DR module source
│   ├── search.c                # Search module source
│   └── update_DR.c             # Update DR module source
│
├── Objects/
│   ├── main_DR.a               # Main DR object/archive
│   ├── display_DR.o            # Display module object
│   ├── No_wilditions.o         # No wilditions object
│   ├── main.a                  # Main program object/archive
│   ├── save_DR.a               # Save DR object/archive
│   ├── search.a                # Search object/archive
│   └── update_DR.a             # Update DR object/archive
│
├── Data/
│   ├── main.db                 # Database file
│   └── save_READ               # Saved read data or configuration
│
├── Modules/
│   ├── Insert_date             # Date insertion module (directory or placeholder)
│   ├── insert_date             # Alternative date insertion module
│   └── inserted_search         # Inserted search module
│
└── Miscellaneous/
    ├── calms                   # Configuration or metadata
    ├── Flat                    # Flat data or resources
    ├── Glad                    # Glad module or resources
    └── Elite                   # Elite module or resources
```

---

## 🚀 Features

- 🔠 Indexes all unique words from multiple input files
- 🔍 Enables fast search for any word across indexed files
- 💾 Save and restore the index database
- 🔄 Supports dynamic file and word updates
- 🧱 Built using hash tables, linked lists, and modular C code

---

## 🧠 How It Works

- **Word Extraction:** Each file is read and every valid word is extracted.
- **Hashing:** Words are hashed to reduce search time and collisions are managed via chaining.
- **Inverted Index:** Each word maps to a list of files and occurrences (line numbers, frequency).
- **Searching:** The user can query a word, and the tool shows its existence across all indexed files.

---

## 🧪 Usage Example

```bash
./output.exe file1.txt file2.txt file3.txt
```

### Interactive Menu Options

```
1. Create Database
2. Display Database
3. Search Word
4. Save Database
5. Update Database
6. Exit
```

### Sample Output

```bash
Enter word to search: algorithm
Found in: file1.txt [line 23], file3.txt [line 7]
```

---

## 🛠️ Build & Run

### Requirements

- GCC compiler
- `make` utility (optional)

### Compile

```bash
cd Project/
make
```

### Run

```bash
./output.exe <file1.txt> <file2.txt> ...
```

---

## 🧹 Cleaning Up

To remove object files and archives:

```bash
make clean
```

---

## 🤝 Contributing

1. Fork this repository
2. Create a branch: `git checkout -b feature/your-feature`
3. Commit your changes
4. Push to GitHub
5. Open a pull request 🚀

---

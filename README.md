# Simple Text Editor C++

A lightweight console-based text editor built in C++ featuring undo/redo functionality, file operations, and text manipulation capabilities.

## Features

- **Line-by-line text input** - Add text lines interactively
- **Undo/Redo** - Full undo and redo support using stack-based state management
- **File Operations** - Save and load text files
- **Find Text** - Search for text within the document
- **Edit Lines** - Modify specific lines by line number
- **Colorful UI** - ANSI color-coded console interface

## Data Structures Used

| Structure | Purpose |
|-----------|---------|
| `vector<string>` | Stores the document lines |
| `stack<vector<string>>` | Manages undo history |
| `stack<vector<string>>` | Manages redo history |

## Commands

| Command | Description |
|---------|-------------|
| `:undo` | Undo the last change |
| `:redo` | Redo a previously undone change |
| `:find [text]` | Search for text in the document |
| `:edit [line_number]` | Edit a specific line |
| `:save [filename]` | Save the document (optional filename) |
| `:load [filename]` | Load a file into the editor |
| `:exit` | Exit the editor |

## How to Use

1. **Compile the program:**
   ```bash
   g++ "text Editor.cpp" -o texteditor
   ```

2. **Run the executable:**
   ```bash
   ./texteditor
   ```

3. **Start typing** - Each line you enter (followed by Enter) will be added to the document.

4. **Use commands** - Type any command starting with `:` to perform operations.

## Example Usage

```
> Hello, World!
> This is my first document.
> :save myfile.txt
 >> Success: File saved to 'myfile.txt'!
> :edit 1
 >> Editing Line 1: Hello, World!
 >> New Text: Hello, Universe!
> :undo
 >> Undid last change.
> :find World
 >> Found 'World' at line 1
> :exit
```

## Limitations

- Maximum of 15 lines displayed at a time
- Console-based interface (requires terminal with ANSI color support)
- Single document editing (no multiple tabs/buffers)

## Requirements

- C++ compiler with C++11 support or higher
- Windows OS (uses `cls` for screen clearing)

## Project Structure

```
Final Project/
├── text Editor.cpp    # Main source code
├── README.md          # This file
└── *.txt              # Saved text files
```

## Author

DSA Project - 3rd Semester

## License

This project is for educational purposes.

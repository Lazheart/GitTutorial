# Basic Terminal Commands 🖥️

This document is a quick guide to learning some essential commands you can use in Git terminal. If you're just starting with the command line, this is for you!

---

## 📁 `cd` - Change Directory

```bash
cd directory_name
```

- Moves you into the specified directory.  
- `cd ..` takes you to the previous directory.  
- `cd` with no arguments takes you to your home directory.

**Example:**

```bash
cd Documents
cd ..
cd ~/Desktop
```

---

## 📄 `ls` - List Files and Folders

```bash
ls
ls -l
ls -a
```

- `ls`: shows the files and folders in the current directory.  
- `-l`: shows details like permissions and dates.  
- `-a`: includes hidden files (those starting with `.`).

**Example:**

```bash
ls -la
```

---

## 📄 `touch` - Create a New File

```bash
touch filename.txt
```

- Creates an empty file with the given name.  
- If the file already exists, it updates the **last modified** timestamp without changing the content.

**Example:**

```bash
touch notes.txt
touch index.html
```
---
## 🧼 `clear` - Clear the Terminal

```bash
clear
```

- Clears all visible text in the terminal.

---

## 📖 `cat` - Display File Content

```bash
cat file.txt
```

- Displays the content of the file directly in the terminal.

---

## ✂️ `mv` - Move or Rename Files and Folders

### Rename:

```bash
mv file.txt new_name.txt
```

### Move file to another folder:

```bash
mv file.txt DestinationFolder/
```

**Example:**

```bash
mv notes.txt ../Documents/
mv old_folder new_name
```

---

## 🗑️ `rm` - Delete Files

```bash
rm file.txt
```

- Deletes a file. ⚠️ There's no recycle bin!

### Delete folder and all its content:

```bash
rm -r Folder
```

---

## ✍️ `vim` - Text Editor in the Terminal

```bash
vim file.txt
```

### Basic Steps:

1. Press `i` to **enter edit mode**.  
2. Type or edit the content.  
3. Press `Esc` to exit edit mode.  
4. Type `:w` to **save**.  
5. Type `:q` to **quit**.  
6. Or type `:wq` to **save and quit**.

### Quit without saving:

```bash
:q!
```

---

> 💡 Tip: If you get lost in `vim`, press `Esc` a few times and type `:q!` to exit without saving.

---

## ✅ All Set!

With these commands, you can navigate, edit, move, and delete files from the terminal. Practice carefully and don’t be afraid to make mistakes!

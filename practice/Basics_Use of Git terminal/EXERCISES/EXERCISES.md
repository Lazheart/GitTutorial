# 🧪 Terminal Exercises

#### 📁 Navigation

1. Navigate to the project folder called `Basics_Use of Git terminal`.  
2. List all files and folders in the current directory, including hidden ones.  
3. Display the contents of the folder `PUT_HERE/`.  

---

#### 📄 File Management

4. Rename the file `CHANGE_MY_NAME.txt` to `CHANGED.txt`.  
5. Delete the file named `DELETE.txt`.  
6. Create a new file named `new_notes.md`.  
7. Create a hidden file called `.logfile.txt`.  

---

#### 🕵️ Hidden Files

8. Find the hidden file in the current directory.  
   > Hint: Use a command that reveals hidden files.  
9. Move the hidden file `.hiddenfile.txt` into the `PUT_HERE/` folder.  
10. Show all files (including hidden ones) inside the `PUT_HERE/` folder.  

---

#### 📜 Viewing Content

11. Display the contents of the file `print.py`.  

---

### ✅ Solutions

```bash
# 1. Navigate to the project folder
cd Basics_Use\ of\ Git\ terminal
```
> `cd` changes the current directory.

```bash
# 2. List all files, including hidden ones
ls -a
```
> `-a` shows hidden files (those starting with a dot).

```bash
# 3. List contents of the PUT_HERE/ folder
ls PUT_HERE/
```
> Shows only visible files inside the specified folder.

```bash
# 4. Rename a file
mv CHANGE_MY_NAME.txt CHANGED.txt
```
> `mv` is used to rename or move files and folders.

```bash
# 5. Delete a file
rm DELETE.txt
```
> `rm` permanently deletes a file.

```bash
# 6. Create a new file
touch new_notes.md
```
> `touch` creates an empty file.

```bash
# 7. Create a hidden file
touch .logfile.txt
```
> Files starting with a `.` are hidden in Unix-like systems.

```bash
# 8. Find hidden files
ls -a
```
> Again, `-a` shows all files, including hidden ones.

```bash
# 9. Move hidden file into another folder
mv .hiddenfile.txt PUT_HERE/
```
> Moves the hidden file into the `PUT_HERE/` folder.

```bash
# 10. Show hidden files in a specific folder
ls -a PUT_HERE/
```
> Shows all files (including hidden) inside `PUT_HERE/`.

```bash
# 11. Display file contents
cat print.py
```
> `cat` prints the content of a file in the terminal.

---

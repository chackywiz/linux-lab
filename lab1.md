````markdown
# 🐧 Assignment 1 – Unit-1: Linux Basics  

**🎯 Objective:** Practice essential Linux commands and run sample lab scripts (Lab3 & Lab5).  

---

## 📂 Selected Lab Files
- ✅ Lab3.sh  
- ✅ Lab5.sh  

---

## ⚙️ Commands, Outputs & Explanations  

---

### 🔹 1. `pwd` – Print Working Directory
**Command:**
```bash
pwd
````

**Output:**

```bash
/home/student/Unit-1
```

**Explanation:**
Prints the **current working directory**. Useful for confirming location before running scripts.

---

### 🔹 2. `ls` – List Directory Contents

**Command:**

```bash
ls
```

**Output (sample):**

```bash
Lab3.sh  Lab5.sh  Documents  Downloads  Pictures  Videos
```

**Explanation:**
Lists files and folders in the current directory. With `-l` it shows detailed info, and with `-a` it shows hidden files.

---

### 🔹 3. `mkdir` – Make Directory

**Command:**

```bash
mkdir testfolder
ls
```

**Output (sample):**

```bash
Lab3.sh  Lab5.sh  testfolder
```

**Explanation:**
Creates a new directory (folder).

---

### 🔹 4. `cd` – Change Directory

**Command:**

```bash
cd testfolder
pwd
```

**Output:**

```bash
/home/student/Unit-1/testfolder
```

**Explanation:**
Moves between directories. `cd ..` goes back, `cd ~` returns to home.

---

### 🔹 5. `rmdir` – Remove Directory

**Command:**

```bash
rmdir testfolder
```

**Output:**

```bash
(no output if successful)
```

**Explanation:**
Removes an **empty directory**.

---

### 🔹 6. `touch` – Create Empty File

**Command:**

```bash
touch file1.txt
ls
```

**Output:**

```bash
file1.txt  Lab3.sh  Lab5.sh
```

**Explanation:**
Creates an empty file or updates timestamp.

---

### 🔹 7. `cp` – Copy File

**Command:**

```bash
cp file1.txt file2.txt
ls
```

**Output:**

```bash
file1.txt  file2.txt  Lab3.sh  Lab5.sh
```

**Explanation:**
Copies files. With `-r` it can copy directories.

---

### 🔹 8. `mv` – Move or Rename File

**Command:**

```bash
mv file2.txt renamed.txt
ls
```

**Output:**

```bash
file1.txt  renamed.txt  Lab3.sh  Lab5.sh
```

**Explanation:**
Moves files into another folder or renames them.

---

### 🔹 9. `rm` – Remove File

**Command:**

```bash
rm renamed.txt
```

**Output:**

```bash
(no output if successful)
```

**Explanation:**
Deletes a file. With `-r` it can delete folders and contents.

---

### 🔹 10. `cat` – View File Content

**Command:**

```bash
cat file1.txt
```

**Output (sample):**

```bash
Hello Linux
```

**Explanation:**
Displays the contents of a file in the terminal.

---

### 🔹 11. `nano` – Open File in Text Editor

**Command:**

```bash
nano file1.txt
```

**Explanation:**
Opens file in **nano editor**. Save with `CTRL+O`, exit with `CTRL+X`.

---

### 🔹 12. `clear` – Clear Terminal

**Command:**

```bash
clear
```

**Explanation:**
Clears the terminal screen. Shortcut: **Ctrl+L**.

---

### 🔹 13. `echo` – Print Text

**Command:**

```bash
echo "Hello World"
```

**Output:**

```bash
Hello World
```

**Explanation:**
Prints text or variables in the terminal.

---

### 🔹 14. `man` – Manual Page

**Command:**

```bash
man ls
```

**Explanation:**
Opens the manual for a command. Press **q** to quit.

---

### 🔹 15. `whoami` – Current User

**Command:**

```bash
whoami
```

**Output:**

```bash
student
```

**Explanation:**
Displays the currently logged-in user.

---

### 🔹 16. `who` – Logged-in Users

**Command:**

```bash
who
```

**Output (sample):**

```bash
student   tty7   2025-09-09 08:32 (:0)
```

**Explanation:**
Shows who is currently logged into the system.

---

### 🔹 17. `passwd` – Change Password

**Command:**

```bash
passwd
```

**Explanation:**
Prompts to change your password.

---

### 🔹 18. `sudo` – Run as Admin

**Command:**

```bash
sudo ls /root
```

**Output (if allowed):**

```bash
rootfiles  secrets.txt
```

**Explanation:**
Runs commands with **root (admin) privileges**.

---

### 🔹 19. `find` – Search for Files

**Command:**

```bash
find . -name "*.txt"
```

**Output:**

```bash
./file1.txt
```

**Explanation:**
Finds files and directories matching a pattern.

---

### 🔹 20. `grep` – Search Inside Files

**Command:**

```bash
grep "Hello" file1.txt
```

**Output:**

```bash
Hello Linux
```

**Explanation:**
Searches for text patterns inside files.

---

## 🧪 Lab File Execution

### 🔹 Lab3.sh

**Command:**

```bash
cat Lab3.sh
```

**Output:**

```bash
#!/bin/bash
echo "Hello, Linux World!"
```

**Run Script:**

```bash
./Lab3.sh
```

**Output:**

```bash
Hello, Linux World!
```

**Explanation:**
A simple shell script that prints a message.

---

### 🔹 Lab5.sh

**Command:**

```bash
cat Lab5.sh
```

**Output:**

```bash
#!/bin/bash
echo "Today is:"
date
```

**Run Script:**

```bash
./Lab5.sh
```

**Output (sample):**

```bash
Today is:
Tue Sep  9 20:45:02 IST 2025
```

**Explanation:**
Script prints today’s date and time using the `date` command.

---

## ❓ Extra Questions

**Q1. Difference between `chmod` and `chown`?**

* `chmod` → Changes file **permissions** (read/write/execute).
* `chown` → Changes file **ownership** (user/group).

**Q2. How do you check current directory and user?**

```bash
pwd       # shows current directory
whoami    # shows current user
```

---

## ✅ Conclusion

This lab covered:

* **Basic Linux commands** (navigation, file handling, editing, search, user management).
* **Lab scripts (Lab3 & Lab5)** for execution practice.
* Differences between **permissions** and **ownership**.

These form the **foundation of Linux usage** for all future labs.

---

```

---



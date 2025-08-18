
---

# basic commands in linux

---

## **1. Basic Navigation Commands**

### `pwd` – Print Working Directory

👉 Shows the current location in the filesystem.

```bash
$ pwd
/home/kali
```

---

### `ls` – List Directory Contents

👉 Lists files and folders in the current directory.

```bash
$ ls
chanu  chanu.c  Desktop  Documents  Downloads  helloworld  helow  helow.c  helow.cy  ls  moksh.c  Music  mycode.c  MYCPprogram  nano.35621.save  Pictures  Public  second  second.c  second.c.save  Templates  Videos  y
                                                                                                                              
```

Options:

* `ls -l` → detailed list with permissions, size, and date
* `ls -a` → show hidden files

---

### `mkdir` – Make Directory

👉 Creates a new directory (folder).

```bash
$ mkdir chanika
$ ls
chanika  chanu  chanu.c  Desktop  Documents  Downloads  helloworld  helow  helow.c  helow.cy  ls  moksh.c  Music  mycode.c  MYCPprogram  nano.35621.save  Pictures  Public  second  second.c  second.c.save  Templates  Videos  y
```

---

### `cd` – Change Directory

👉 Moves between directories.

```bash
$ cd chanika
$ pwd
/home/kali/chanika
```

To go back one level:

```bash
$ cd ..
```

To go to home directory:

```bash
$ cd ~
```

---

### `rmdir` – Remove Directory

👉 Deletes an **empty directory**.

```bash
$ rmdir chanika
```

---

## **2. File Operations**

### `touch` – Create Empty File

👉 Creates an empty file or updates its timestamp.

```bash
$ touch file1.txt
$ ls
file1.txt
```

---

### `cp` – Copy File/Directory

👉 Copies files.

```bash
$ cp file1.txt 
```

👉 Copy a folder:

```bash
$ cp -r folder1 folder_copy
```

---

### `mv` – Move or Rename File/Directory

👉 Move file to another folder:

```bash
$ mv file1.txt folder1/
```

👉 Rename file:

```bash
$ mv copy.txt renamed.txt
```

---

### `rm` – Remove File/Directory

👉 Delete a file:

```bash
$ rm file1.txt
```

👉 Delete a folder with contents:

```bash
$ rm -r folder1
```

---

## **3. File Viewing and Editing**

### `cat` – View File Content

👉 Prints contents of a file.

```bash
$ cat file1.txt
Hello Linux
```

---



### `nano` – Text Editor

👉 Open file for editing inside terminal.

```bash
$ nano file1.txt
```

* Save: `CTRL + O`
* Exit: `CTRL + X`

---
### 'clear' -clears the terminal

```bash
clear
```
shortcut: ctrl+L

### ' cat' - view file contents

Displays content in terminal.

```bash
$ cat file.txt
```

### 'echo' - print texts

```bash
$ echo "hello world"
```

### ' man' - manual for any command


```bash
$ man ls
```

Use q to quit the manual.


---

## **4. User Management**

### `whoami` – Current User

```bash
$ whoami
kali
```

---

### `who` – Logged-in Users

```bash
$ who
kali     tty7         2025-08-18 03:25 (:0)
```

---



### `passwd` – Change Password

👉 Prompts for new password.

```bash
$ passwd
```

---

### `sudo` – Run as Admin

👉 Run command with root privileges.

```bash
$ sudo ls /root
```

---

## **5. SEARCH AND FINDINGS **

### 'find' -locate files

```bash
$ find . -name "*.txt"
```
Finds all .txt files in current folder and subfolders

---

### grep - search inside files

```bash
$ grep "hello" file1.txt
```

# ✅ Conclusion

These commands form the **foundation of Linux usage**. They cover:

* Navigation (`pwd`, `ls`, `cd`, `mkdir`, `rmdir`)
* File handling (`touch`, `cp`, `mv`, `rm`)
* Viewing/editing (`cat`, `nano`, `vim`)
* User management (`whoami`, `who`, `passwd`, `sudo`)
* search and findings (`find`, 'grep')

---

👉 Do you want me to also turn **these notes with examples** into a **clean PDF (like ready-to-upload notes)** just like I did with your experiment report?

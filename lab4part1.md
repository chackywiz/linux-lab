

# 📘 Advanced Linux File Commands 

---

## **1. File Manipulation Commands**

### 🔹 `touch` – Create or Update File

```bash
touch file.txt        # Create empty file
touch file1 file2     # Create multiple files
touch existing.txt    # Update timestamp of an existing file
```

📌 **Note:** If the file exists, `touch` only updates its timestamp.

---

### 🔹 `cp` – Copy Files & Directories

```bash
cp file1.txt file2.txt         # Copy file
cp file.txt /home/user/        # Copy file to another directory
cp -r dir1 dir2                # Copy directory recursively
cp -p file.txt backup.txt      # Preserve timestamps & permissions
```

📌 **Tip:** Use `-i` to confirm before overwriting.

---

### 🔹 `mv` – Move or Rename Files

```bash
mv old.txt new.txt             # Rename file
mv file.txt /home/user/        # Move file
mv -f file.txt /backup/        # Force move (overwrite without prompt)
```

---

### 🔹 `rm` – Remove Files & Directories

```bash
rm file.txt                    # Delete file
rm file1 file2                 # Delete multiple files
rm -r folder/                  # Delete folder recursively
rm -rf folder/                 # Force delete (no prompt)
```

⚠️ **Warning:** Use with care! Deleted files are not easily recoverable.

---

### 🔹 `cat` – View & Concatenate Files

```bash
cat file.txt                   # Display file contents
cat file1 file2 > combined.txt # Merge files
cat -n file.txt                # Show with line numbers
```

---

### 🔹 `less` – View File Page by Page

```bash
less file.txt
```

🔹 **Navigation in `less`**

* `Space` → Next page
* `b` → Previous page
* `/word` → Search forward
* `q` → Quit

---

### 🔹 `head` – Show Start of File

```bash
head file.txt                  # Show first 10 lines
head -n 20 file.txt            # Show first 20 lines
```

### 🔹 `tail` – Show End of File

```bash
tail file.txt                  # Show last 10 lines
tail -n 15 file.txt            # Show last 15 lines
tail -f logfile.txt            # Monitor file updates live
```

---

## **2. File Permissions & Ownership**

### 🔹 Viewing Permissions

```bash
ls -l
```

**Example output:**

```
-rw-r--r-- 1 user group 1024 Aug 19 12:00 file.txt
```

* `rw-` → Owner (read, write)
* `r--` → Group (read)
* `r--` → Others (read)

---

### 🔹 `chmod` – Change Permissions

**Symbolic Method:**

```bash
chmod u+x script.sh     # Add execute for owner
chmod g-w file.txt      # Remove write for group
chmod o+r notes.txt     # Add read for others
```

**Numeric Method (r=4, w=2, x=1):**

```bash
chmod 755 script.sh     # rwxr-xr-x
chmod 644 file.txt      # rw-r--r--
```

---

### 🔹 `chown` – Change File Owner

```bash
sudo chown user file.txt        # Change owner
sudo chown user:group file.txt  # Change owner & group
```

### 🔹 `chgrp` – Change Group

```bash
sudo chgrp developers file.txt
```

---

## **3. Advanced Operations**

### 🔹 `find` – Search for Files

```bash
find /home -name "file.txt"       # Search by name
find /home -name "*.log"          # Search by extension
find /var -size +100M             # Find files >100MB
find /tmp -name "*.tmp" -delete   # Find & delete
find . -name "*.txt" -exec rm {} \;  # Run command on result
```

---

### 🔹 `grep` – Search Text in Files

```bash
grep "error" logfile.txt          # Search word
grep -i "error" logfile.txt       # Case-insensitive
grep -r "TODO" project/           # Recursive search
grep -n "warning" logfile.txt     # Show line numbers
grep --color=auto "error" file    # Highlight matches
```

---

### 🔹 `tar` – Archiving

```bash
tar -cvf archive.tar file1 dir/   # Create archive
tar -xvf archive.tar              # Extract archive
tar -tvf archive.tar              # View archive
tar -czvf archive.tar.gz dir/     # Create compressed archive
tar -xzvf archive.tar.gz          # Extract compressed archive
```

---

### 🔹 `gzip` & `gunzip` – Compression

```bash
gzip file.txt       # Compress → file.txt.gz
gunzip file.txt.gz  # Decompress
```

---

### 🔹 `ln` – Links

```bash
ln file.txt hardlink.txt          # Hard link
ln -s /path/original symlink.txt  # Symbolic (soft) link
```

---

## **4. Useful Extra Commands**

```bash
stat file.txt         # Detailed file info (timestamps, inode)
wc -l file.txt        # Count lines
du -sh folder/        # Show folder size
df -h                 # Show disk usage
nano file.txt         # Edit file in Nano
```

---

✅ This version is now **polished, organized, and ready-to-study**. It reads like a proper set of lab notes.

Do you want me to **make this into a formatted PDF lab report** (with headings, explanations, and placeholders for screenshots of commands) so you can directly submit it in college?

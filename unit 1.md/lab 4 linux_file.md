
# 🐧 Advanced Linux File Commands – My Notes

## **1. File Handling Basics**

### **`touch`** – Create Empty Files / Update Timestamp

```bash
# Make a new file
touch notes.txt

# Update modified time of an existing file
touch report.docx

# Create many files together
touch day1.txt day2.txt day3.txt
```

---

### **`cp`** – Copy Files and Folders

```bash
# Copy one file
cp hello.txt copy_hello.txt

# Copy to another folder
cp hello.txt ~/Documents/

# Copy folder with everything inside
cp -r Project BackupProject

# Keep same attributes (time, permissions)
cp -p resume.pdf resume_backup.pdf
```

---

### **`mv`** – Move / Rename Files

```bash
# Rename a file
mv draft.txt final.txt

# Move file into another folder
mv final.txt ~/Desktop/

# Force move (overwrite if already exists)
mv -f notes.txt ~/Downloads/
```

---

### **`rm`** – Delete Files and Folders

```bash
# Remove single file
rm temp.txt

# Remove multiple files
rm file1 file2

# Remove whole directory
rm -r old_project/

# Force delete without asking
rm -rf old_logs/
```

---

### **`cat`** – Show / Combine Files

```bash
# Print contents
cat story.txt

# Merge 2 files into one
cat part1.txt part2.txt > complete.txt

# Show file with line numbers
cat -n script.sh
```

---

### **`less`** – Read File Page by Page

```bash
less bigfile.txt
# Keys:
# Space → next page
# b → back page
# q → quit
```

---

### **`head`** – First Few Lines

```bash
# First 10 lines (default)
head log.txt

# First 25 lines
head -n 25 log.txt
```

---

### **`tail`** – Last Few Lines

```bash
# Last 10 lines (default)
tail log.txt

# Last 50 lines
tail -n 50 log.txt

# Live monitor file changes
tail -f system.log
```

---

## **2. Permissions & Ownership**

### **`ls -l`** – Detailed View

```bash
ls -l
# Example:
# -rwxr--r-- 1 chaya devs 2048 Sep 09 08:00 hello.sh
# Meaning:
# [1] -rwxr--r-- → permissions
# [2] 1 → hard link count
# [3] chaya → owner
# [4] devs → group
# [5] 2048 → file size (bytes)
# [6] Sep 09 08:00 → modified date
# [7] hello.sh → file name
```

---

### **Permission Groups**

* **Owner (u)** → file creator
* **Group (g)** → group members
* **Others (o)** → all other users
* Permissions: **r (read), w (write), x (execute)**

---

### **`chmod`** – Change Permissions

```bash
# Symbolic way
chmod u+x run.sh    # give owner execute
chmod g-w notes.txt # remove group write
chmod o+r notes.txt # give others read

# Numeric way (r=4, w=2, x=1)
chmod 755 run.sh    # rwxr-xr-x
chmod 644 notes.txt # rw-r--r--
```

---

### **`chown`** – Change Owner

```bash
# Change file owner
sudo chown me file1.txt

# Change owner + group
sudo chown me:staff file1.txt
```

---

### **`chgrp`** – Change Group

```bash
sudo chgrp admin project.docx
```

---

## **3. Advanced Operations**

### **`find`** – Search Files

```bash
# Find by name
find ~/Documents -name "todo.txt"

# Find all .log files
find /var -name "*.log"

# Find bigger than 200 MB
find / -size +200M

# Find & delete together
find . -name "*.bak" -delete
```

---

### **`grep`** – Search Inside Files

```bash
# Simple search
grep "fail" server.log

# Ignore case
grep -i "error" app.log

# Search whole folder
grep -r "FIXME" ~/Projects/

# Show line numbers
grep -n "done" tasks.txt
```

---

### **`tar`** – Archiving

```bash
# Create tar
tar -cvf backup.tar notes.txt images/ project/

# Extract tar
tar -xvf backup.tar

# Just list contents
tar -tvf backup.tar
```

---

### **`gzip` & `gunzip`** – Compress / Decompress

```bash
# Compress (creates .gz)
gzip report.pdf

# Decompress
gunzip report.pdf.gz
```

---

### **`ln`** – Links

```bash
# Hard link
ln data.txt data_hard.txt

# Soft (symbolic) link
ln -s /var/log/syslog loglink
```

---


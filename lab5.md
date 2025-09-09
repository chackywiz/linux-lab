

---

# 📜 `starter_kit.sh`

```bash
#!/bin/bash
# starter_kit.sh
# Script to set up a starter project structure

# Create folder structure
mkdir -p project/scripts
mkdir -p project/docs
mkdir -p project/data

# Add placeholder README.md in each folder
echo "# Scripts Folder" > project/scripts/README.md
echo "# Documentation Folder" > project/docs/README.md
echo "# Data Folder" > project/data/README.md
echo "# Main Project Folder" > project/README.md

# Print completion message
echo "✅ Starter Kit Ready!"
```

---

# 📄 LAB\_extra.md – Starter Kit & Automation

---

# 🖥️ Lab 5 – Starter Kit & Automation

## 🎯 Objective

To automate the creation of a **starter project environment** with predefined folders and README files, ensuring consistent structure for new projects.

---

## **1. Script Explanation (`starter_kit.sh`)**

```bash
mkdir -p project/scripts
mkdir -p project/docs
mkdir -p project/data
```

👉 Creates project folders.

* `-p` ensures parent directories are created if they don’t exist.

```bash
echo "# Scripts Folder" > project/scripts/README.md
echo "# Documentation Folder" > project/docs/README.md
echo "# Data Folder" > project/data/README.md
echo "# Main Project Folder" > project/README.md
```

👉 Adds placeholder `README.md` in each folder so structure is clear.

```bash
echo "✅ Starter Kit Ready!"
```

👉 Prints success message when setup is done.

---

## **2. Example Run**

### ▶ Run Script

```bash
$ ./starter_kit.sh
✅ Starter Kit Ready!
```

### 📂 Project Structure After Run

```bash
project/
├── README.md
├── scripts/
│   └── README.md
├── docs/
│   └── README.md
└── data/
    └── README.md
```

---

## **3. Extra Questions**

### 🔹 Q1: What does `mkdir -p` do?

* Creates directories **recursively**.
* If parent folder doesn’t exist, it will be created automatically.
* Prevents errors if directory already exists.

Example:

```bash
mkdir -p project/scripts
```

Creates both `project/` and `scripts/` if they don’t exist.

---

### 🔹 Q2: Why is automation useful in DevOps?

* Ensures **consistency** → same setup every time.
* Saves **time** → no need to manually create folders/files.
* Reduces **human error**.
* Core principle of DevOps: **automate repetitive tasks** like setup, deployment, and monitoring.

---

## ✅ Conclusion

* Built `starter_kit.sh` to automatically generate a project structure.
* Confirmed via example run that all folders & README files are created.
* Learned importance of **automation** in DevOps workflows.

---

📌 **Deliverables**:

* `starter_kit.sh` (script)
* `LAB_extra.md` (this report)
* PDF version for submission

---

.

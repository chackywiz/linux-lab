

---

# 🧪 Practice Experiment – Users & Groups in Linux

### 🔹 **1. Create a New User**

```bash
sudo useradd -m riya
```

* `-m` → Creates a home directory `/home/riya`.

---

### 🔹 **2. Create a New Group**

```bash
sudo groupadd devteam
```

---

### 🔹 **3. Add the User to the Group**

```bash
sudo usermod -aG devteam riya
```

* `-aG` → Append user to the group (keeps existing groups intact).

---

### 🔹 **4. Create a File (as current user)**

```bash
touch project.txt
```

Check ownership:

```bash
ls -l project.txt
```

Example output:

```
-rw-r--r-- 1 priya priya 0 Sep 9 15:20 project.txt
```

---

### 🔹 **5. Change File Ownership**

Assign file ownership to **`riya`** and group **`devteam`**:

```bash
sudo chown riya:devteam project.txt
```

---

### 🔹 **6. Verify Ownership**

```bash
ls -l project.txt
```

Output:

```
-rw-r--r-- 1 riya devteam 0 Sep 9 15:20 project.txt
```

---

✅ Now, **user `riya` (in group `devteam`) owns `project.txt`**.

---



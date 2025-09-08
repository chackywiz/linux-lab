

# 👥 Linux Users & Groups Access Management Commands

## ✅ 1. **Users in Linux**

A **user** in Linux represents an account that can log in and interact with the system. Each user has specific **permissions** that control what they can access.

### 🔑 Types of Users

1. **Root User (Superuser)**

   * **Username**: `root`
   * **UID**: `0` (always reserved for root)
   * **Role**: Full control over the system. Can install/remove packages, change system configs, and access all files.

2. **Normal User**

   * Regular login accounts for people.
   * **UID**: Usually starts from `1000` (depends on distribution).
   * **Privileges**: Limited to their home directory and files they own. Can’t modify system files unless given `sudo` access.

3. **System User**

   * **UID**: Typically lower than `1000`.
   * **Role**: Used by background services (e.g., `mysql`, `www-data`).
   * **Privileges**: Restricted to what the service needs.

---

## ✅ 2. **Groups in Linux**

A **group** is a way to manage permissions for multiple users at once.

### 🔑 Types of Groups

1. **Primary Group**

   * Every user has a primary group by default.
   * Example: If you create a user `chaya`, the system also makes a primary group called `chaya`.

2. **Secondary Groups**

   * Users can be added to multiple groups for extra access.
   * Example: `chaya` may also belong to the group `developers`.

3. **System Groups**

   * Special groups for services.
   * Example: `www-data` (for web servers), `mysql` (for databases).

---

## ✅ 3. **Creating & Managing Users & Groups**

### 👤 Create a New User

```bash
sudo adduser chaya
```

This creates the user **chaya** and her primary group.

### 👥 Create a New Group

```bash
sudo groupadd devteam
```

Creates a group named **devteam**.

---

### ➕ Add a User to a Group

```bash
sudo usermod -aG devteam chaya
```

Adds **chaya** to the **devteam** group.

---

### 🔄 Change User’s Primary Group

```bash
sudo usermod -g admin chaya
```

Changes **chaya**’s primary group to **admin**.

---

### 📜 List All Users

```bash
cat /etc/passwd
```

Shows all user accounts with details like UID, home directory, and shell.

---

### 📜 List All Groups

```bash
cat /etc/group
```

Displays all groups and their members.

---

## ✅ 4. **File Permissions & Groups**

Linux permissions control who can **read, write, or execute** files.

Example:

```bash
-rwxr-xr--
```

* **Owner**: `rwx` → read, write, execute
* **Group**: `r-x` → read, execute
* **Others**: `r--` → read only

### 👑 Change Group Ownership of a File

```bash
sudo chown :devteam project.txt
```

Now the group **devteam** owns `project.txt`.

---

## ✅ 5. **User IDs (UIDs) & Group IDs (GIDs)**

* **UID 0** → Root
* **UID ≥ 1000** → Regular users
* **GID 0** → Root group
* **GID ≥ 1000** → Normal groups

### 🔎 Check a User’s UID/GID

```bash
id chaya
```

Shows UID, GID, and all groups for **chaya**.

---

## ✅ 6. **Special Groups in Linux**

* **`sudo` / `wheel`** → Run commands as root.
* **`www-data`** → Web server user/group.
* **`staff`** → macOS group with extra privileges.
* **`admin`** → Extra admin rights (depends on distro).

---

## ✅ 7. **Deleting Users & Groups**

### ❌ Delete a User + Home Directory

```bash
sudo deluser --remove-home chaya
```

---

### ❌ Delete a Group

```bash
sudo delgroup devteam
```

---

## 📌 Summary

* **Users** = accounts that log in (root, normal, system).
* **Groups** = collections of users for easier permission management.
* **Permissions** are managed with users & groups (`chmod`, `chown`).
* **Root & sudo** users have full system control.

---



---

## ✅ **1. Users in Linux**

A **user** in Linux represents an account that can log in, own files, and run processes.

### Types of Users:

1. **Root User (Superuser)**

   * **Username**: `root`
   * **UID**: `0`
   * **Role**: Complete control over the system.
   * Can modify/delete any file and manage all users.

2. **Normal User**

   * Example: `chayanika` (created during system setup or manually).
   * **UID**: Typically starts from `1000`.
   * **Role**: Manage personal files, run applications, limited access to system files.
   * **Home Directory**: `/home/chayanika`

3. **System User**

   * Used by background services (`www-data`, `mysql`, etc.).
   * Typically has **UID < 1000**.
   * Does not log in interactively.

---

## ✅ **2. Groups in Linux**

A **group** is a collection of users. Helps manage permissions efficiently.

### Types of Groups:

1. **Primary Group**

   * Created with the same name as the user.
   * For `chayanika`, the primary group is usually `chayanika`.

2. **Secondary Groups**

   * Additional groups that a user can join.
   * Example: `chayanika` may also be part of `developers`.

3. **System Groups**

   * Special groups for services (e.g., `www-data`, `mysql`).

---

## ✅ **3. Managing Users & Groups**

### **Create a New User**

```bash
sudo adduser chayanika
```

Creates a new user with a home directory `/home/chayanika`.

### **Create a New Group**

```bash
sudo groupadd developers
```

### **Add User to a Group**

```bash
sudo usermod -aG developers chayanika
```

Adds **`username`** to the `developers` group.

### **Change Primary Group**

```bash
sudo usermod -g admin chayanika
```

Changes **primary group** of `username` to `admin`.

---

## ✅ **4. Listing Users & Groups**

### List All Users

```bash
cat /etc/passwd
```

### List All Groups

```bash
cat /etc/group
```

### View `username`’s Groups and IDs

```bash
id chayanika
```

Example output:

```
uid=1001(chayanika) gid=1001(chayanika) groups=1001(chayanika),1002(developers),27(sudo)
```

---

## ✅ **5. File Permissions and Groups**

### Example:

```bash
-rwxr-xr--
```

* **Owner (chayanika)**: `rwx`
* **Group (developers)**: `r-x`
* **Others**: `r--`

### Change Group Ownership of a File

```bash
sudo chown :developers file.txt
```

### Change File Owner

```bash
sudo chown chayanika file.txt
```

---

## ✅ **6. Default IDs**

* **UID 0** → `root`
* **UID ≥ 1000** → Regular users (e.g., `chayanika`)
* **GID 0** → Root group
* **GID ≥ 1000** → Normal user groups

---

## ✅ **7. Special Groups**

* `sudo` (or `wheel`): members can run `sudo` commands.
  Example: if `chayanika` is in `sudo` group, she can run:

  ```bash
  sudo apt update
  ```
* `www-data`: used by Apache/Nginx web server.
* `staff`: common on macOS.

---

## ✅ **8. Deleting Users & Groups**

### Delete a User and Home Directory

```bash
sudo deluser --remove-home chayanika
```

### Delete a Group

```bash
sudo delgroup developers
```

---

# 🔑 **Summary**

* `username` = Normal Linux user with her own UID and home directory.
* Belongs to **primary group** `username` and can be added to **secondary groups** like `developers`.
* Permissions are managed with `chmod`, ownership with `chown`, and group membership with `usermod`.

---



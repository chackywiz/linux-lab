

---

# 🔑 File Permissions with `chmod` and `chown`

---

## **1. Basics of File Permissions**

Every file/directory in Linux has three permission categories:

* **Owner (u)** → The creator of the file.
* **Group (g)** → Users in the same group.
* **Others (o)** → Everyone else.

### Permission Types

* **r = Read (4)** → View contents
* **w = Write (2)** → Modify or delete
* **x = Execute (1)** → Run as a program

### Example Layout

Output of `ls -l`:

```
-rwxr-xr--
```

Breakdown:

* `-` → Regular file (`d` = directory, `l` = link, etc.)
* `rwx` → Owner has full access
* `r-x` → Group can read & execute
* `r--` → Others can only read

---

## **2. Changing Permissions with `chmod`**

### Syntax

```bash
chmod [options] mode filename
```

Modes can be **numeric (octal)** or **symbolic**.

---

### (A) Numeric (Octal) Method

Values:

* r = 4
* w = 2
* x = 1

Add them up:

* 7 = rwx
* 6 = rw-
* 5 = r-x
* 4 = r--
* 0 = ---

**Example:**

```bash
chmod 755 script.sh
```

Meaning:

* Owner → `rwx`
* Group → `r-x`
* Others → `r-x`

---

### (B) Symbolic Method

* `u` = user (owner)
* `g` = group
* `o` = others
* `a` = all

Operators:

* `+` add
* `-` remove
* `=` set exactly

**Examples:**

```bash
chmod u+x run.sh       # Add execute for owner
chmod g-w notes.txt    # Remove write for group
chmod o=r report.txt   # Others can only read
chmod a+r data.csv     # Everyone gets read access
```

---

### (C) Recursive Changes

```bash
chmod -R 755 mydir/
```

* `-R` = apply to all files/subfolders inside.

---

## **3. Changing Ownership with `chown`**

### Syntax

```bash
chown [options] new_owner:new_group filename
```

**Examples:**

```bash
chown priya file.txt          # Change owner to user 'priya'
chown priya:team file.txt     # Change owner to 'priya' and group to 'team'
chown :team file.txt          # Change only group
chown -R priya:team /project  # Recursive ownership change
```

---

## **4. Example Scenario**

```bash
touch demo.sh
ls -l demo.sh
```

Output:

```
-rw-r--r-- 1 priya team 0 Sep 9 10:00 demo.sh
```

Now:

```bash
chmod 700 demo.sh           # Only owner has rwx
chmod u+x,g-w demo.sh       # Add execute to user, remove write from group
chown root:admin demo.sh    # Change owner to root, group to admin
```

---

## **5. Quick Permission Reference**

| Number | Symbol | Meaning      |
| ------ | ------ | ------------ |
| 0      | ---    | No access    |
| 1      | --x    | Execute only |
| 2      | -w-    | Write only   |
| 3      | -wx    | Write + Exec |
| 4      | r--    | Read only    |
| 5      | r-x    | Read + Exec  |
| 6      | rw-    | Read + Write |
| 7      | rwx    | Full access  |

---

✅ **Pro tip**: Use **numbers** (e.g., `755`, `644`) when setting full permissions, and **symbols** (`u+x`, `g-w`) for quick tweaks.

---


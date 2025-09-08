

# 🐚 Shell Scripting – My Notes

Shell scripting helps us **automate tasks** in Linux by writing commands in a file and letting the shell run them one by one.

---

## 1️⃣ What is a Shell Script?

* A **shell** = command-line program (like `bash`, `zsh`, `sh`).
* A **script** = text file with commands.
* Usually ends with `.sh` but not compulsory.

**Example (`hello.sh`):**

```bash
#!/bin/bash
echo "Hello, Linux!"
```

Run it:

```bash
chmod +x hello.sh   # give execute permission
./hello.sh
```

👉 Output:

```
Hello, Linux!
```

---

## 2️⃣ Variables

Variables = storage for data (name, number, path).

**Define variables:**

```bash
name="Riya"
age=19
```

⚠️ No spaces around `=`.

**Use variables:**

```bash
echo "My name is $name and I am $age years old."
```

👉 Output:

```
My name is Riya and I am 19 years old.
```

**Some built-in variables:**

```bash
echo $HOME   # home directory
echo $USER   # current username
echo $PWD    # current folder
```

---

## 3️⃣ User Input

Ask user for input:

```bash
#!/bin/bash
echo "Enter your favorite subject:"
read subject
echo "You chose $subject"
```

---

## 4️⃣ If-Else (Conditions)

```bash
#!/bin/bash
num=10

if [ $num -gt 5 ]; then
    echo "Number is greater than 5"
else
    echo "Number is less or equal to 5"
fi
```

Operators: `-eq`, `-ne`, `-gt`, `-lt`, `-ge`, `-le`

---

## 5️⃣ Loops

**For Loop:**

```bash
for i in {1..5}
do
    echo "Iteration $i"
done
```

**While Loop:**

```bash
count=1
while [ $count -le 3 ]
do
    echo "Count: $count"
    ((count++))
done
```

**Until Loop:**

```bash
x=1
until [ $x -gt 3 ]
do
    echo "Value: $x"
    ((x++))
done
```

---

## 6️⃣ Functions

Reusable block of code.

```bash
greet() {
    echo "Hello, $1"
}

greet Riya
greet Dev
```

👉 Output:

```
Hello, Riya
Hello, Dev
```

---

## 7️⃣ Command Line Arguments

```bash
#!/bin/bash
echo "Script name: $0"
echo "First arg: $1"
echo "Second arg: $2"
echo "All args: $@"
echo "Total: $#"
```

Run:

```bash
./script.sh apple banana
```

---

## 8️⃣ Arrays

```bash
subjects=("Math" "Physics" "CS")

echo "First: ${subjects[0]}"

for s in "${subjects[@]}"; do
    echo "Subject: $s"
done
```

---

## 9️⃣ Handy Commands

* `date` → current date/time
* `whoami` → current user
* `ls` → list files
* `pwd` → show folder path
* `cat file.txt` → print file contents

---

## 🔟 Small Project – Backup Script

```bash
#!/bin/bash
# Backup home directory into /tmp

backup="/tmp/home_backup_$(date +%Y%m%d%H%M%S).tar.gz"

tar -czf $backup $HOME

echo "Backup stored at $backup"
```

---


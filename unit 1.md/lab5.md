
---

# 🐚 Shell Scripting – My Notes

## **1. What is a Shell Script?**

* A **shell script** is just a text file with a list of commands for the shell to run.
* It helps **automate repetitive tasks** instead of typing them one by one.
* Example uses: running multiple commands together, creating backups, looping over files, etc.

---

## **2. Writing Your First Shell Script**

1. Make a new file:

   ```bash
   nano first.sh
   ```

2. Add this code:

   ```bash
   #!/bin/bash
   # My very first script

   echo "Hey there! This is my first script."
   ```

   * `#!/bin/bash` → called **shebang**, tells Linux to use bash.
   * `echo` → prints output.
   * `#` → comment line (ignored by shell).

3. Save & exit (`CTRL+O`, `CTRL+X` in nano).

4. Give execute permission:

   ```bash
   chmod +x first.sh
   ```

5. Run it:

   ```bash
   ./first.sh
   ```

✅ Output:

```
Hey there! This is my first script.
```

---

## **3. Variables in Shell**

We can store data inside variables:

```bash
#!/bin/bash

student="Chaya"
roll=101

echo "Student name: $student"
echo "Roll number: $roll"
```

⚠️ Note: Don’t put spaces around `=` while assigning.

---

## **4. User Input**

```bash
#!/bin/bash

echo "What’s your favorite color?"
read color

echo "Nice! $color is a beautiful choice."
```

* `read` → lets user enter data.
* `$color` → fetches the input value.

---

## **5. Conditional Statements (if-else)**

```bash
#!/bin/bash

echo "Enter your marks:"
read marks

if [ $marks -ge 40 ]
then
    echo "Congrats, you passed!"
else
    echo "Sorry, better luck next time."
fi
```

* `-ge` → greater than or equal.
* Other operators:

  * `-lt` → less than
  * `-eq` → equal
  * `-ne` → not equal

---



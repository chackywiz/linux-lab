

# 📜 `enhanced_numbers.sh`

```bash
#!/bin/bash
# enhanced_numbers.sh
# Prints numbers from start to end with a given step

# Check if 3 arguments are provided
if [ $# -ne 3 ]; then
  echo "Usage: $0 <start> <end> <step>"
  exit 1
fi

start=$1
end=$2
step=$3

# Validate step > 0
if [ $step -le 0 ]; then
  echo "Error: Step must be a positive number."
  exit 1
fi

# Loop through numbers
for (( i=$start; i<=$end; i+=$step ))
do
  echo "Number: $i"
done
```

---

# 📄 LAB3.md – Modified Script Report

---

# 🖥️ Assignment 3 – Modify an Existing Script

## 🎯 Objective

To enhance `print_numbers.sh` so that it accepts **user input (start, end, step)** and validates the step.

---

## **1. Original Behavior**

The original script simply printed numbers from **1 to 5** without user input:

```bash
#!/bin/bash
for i in {1..5}
do
  echo "Number: $i"
done
```

👉 Limitation: Fixed numbers, no flexibility.

---

## **2. New Behavior (`enhanced_numbers.sh`)**

Now, the script:

* Takes **start, end, step** values from the user.
* Validates that step > 0.
* Prints the sequence accordingly.

---

## **3. Example Runs**

### ✅ Example 1

```bash
$ ./enhanced_numbers.sh 1 10 2
Number: 1
Number: 3
Number: 5
Number: 7
Number: 9
```

### ✅ Example 2

```bash
$ ./enhanced_numbers.sh 5 20 5
Number: 5
Number: 10
Number: 15
Number: 20
```

### ❌ Invalid Example

```bash
$ ./enhanced_numbers.sh 1 10 -2
Error: Step must be a positive number.
```

---

## **4. Extra Questions**

### 🔹 Q1: Difference between `$1`, `$@`, and `$#` in bash?

* `$1` → first argument passed to the script.
* `$@` → all arguments as separate values.
* `$#` → total number of arguments.

Example:

```bash
$ ./script.sh A B C
$1 = A
$@ = A B C
$# = 3
```

---

### 🔹 Q2: What does `exit 1` mean in a script?

👉 `exit 1` stops the script and returns an **error status code (1)** to the system.

* `exit 0` → success.
* Non-zero (like `exit 1`) → error/failure.

---

## ✅ Conclusion

* Original script → fixed loop from 1 to 5.
* Enhanced script → **user-controlled range & step** with input validation.
* Learned: **arguments (\$1, \$@, \$#)** and **exit codes** in bash.

---

📌 **Deliverables**:

* `enhanced_numbers.sh` (script file)
* `LAB3.md` (this explanation)
* Export as **PDF** for submission

---


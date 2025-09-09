# 🖥️ LAB0 – Ubuntu Installation Report  

---

## 📌 1. Installation Method
- **Chosen Method:** Virtual Machine using **Oracle VirtualBox**  
- **Reason:** Allows Ubuntu to run inside Windows without disturbing the host OS.  

---

## ⚙️ 2. Setup & Installation  

### 🔹 Step 1 – VirtualBox VM Creation  
> Created a new VM, selected Ubuntu ISO, allocated **4 GB RAM** and **20 GB storage**.  

![VM Creation](./screenshots/Screenshot%202025-09-09%20193056.png)

---

### 🔹 Step 2 – Ubuntu Installation  
> Booted from ISO, followed on-screen instructions, and installed Ubuntu Desktop.  

![Ubuntu Installation](./screenshots/Screenshot%202025-09-09%20195758.png)  

---

### 🔹 Step 3 – First Login  
> Successfully logged into Ubuntu after installation.  

![First Login](./screenshots/Screenshot%202025-09-09%20202111.png)  

---

## 💻 3. Terminal Commands & Outputs  

Executed basic Linux commands to verify installation:  

| Command           | Purpose                          | Screenshot |
|-------------------|----------------------------------|------------|
| `lsb_release -a`  | Shows Ubuntu version info        | ![lsb_release](./screenshots/Screenshot%202025-09-09%20202643.png) |
| `uname -a`        | Displays kernel & system details | ![uname](./screenshots/Screenshot%202025-09-09%20202708.png) |
| `df -h`           | Checks disk space usage          | ![df](./screenshots/Screenshot%202025-09-09%20202732.png) |
| `free -m`         | Shows memory usage in MB         | ![free](./screenshots/Screenshot%202025-09-09%20202748.png) |

---

## ✍️ 4. Reflection  

During the installation, I faced some challenges:  
- ⏳ **Large ISO Download:** Took time due to slow internet.  
- 🔑 **BIOS Virtualization:** Needed to enable virtualization in BIOS settings.  
- 🐢 **Slow First Boot:** The first boot of Ubuntu in VM was sluggish.  

✅ **Learning Outcome:** I now understand how to install Ubuntu on a VM and verify it using terminal commands.  

---

## 📚 5. Comparative Study  

### ✅ Advantages of **VirtualBox**
1. 🖥️ Can run Ubuntu alongside Windows without restarting.  
2. 🔄 Easy to clone, reset, or restore snapshots if something breaks.  

### ✅ Advantages of **Dual Boot**
1. ⚡ Provides full hardware performance (no VM overhead).  
2. 💻 Best for heavy workloads when Ubuntu is the main OS.  

---

## 📝 Notes  
- 📂 **All screenshots** are stored in the `screenshots/` folder.  
- 📄 This report was created in **Markdown** and exported as **PDF** using the *Markdown PDF* extension in VS Code.  

✨ **Final Result:** A fully working Ubuntu VM ready for future lab tasks! 🚀  

# 🐧 Linux Day 1 – Cloud Maven Training

## 📌 Overview

In this session, I performed hands-on practice of Linux fundamentals including:

- User Management
- File Permissions & Ownership
- Process Management
- Vim Text Editor
- Basic Command Line Operations

All labs were executed on a Linux environment (WSL).

---

# 🧪 Lab 1 – User Management

### 🔹 Create a New User

```bash
sudo adduser devuser
🔹 Switch to the User
   su - devuser
🔹 Verify Home Directory
   pwd

# 🧪 Lab 2 – File Permissions & Ownership
 🔹 Create a File
    touch labfile.txt
 🔹 Check Permissions
    ls -l
 🔹 Change Permissions
    chmod 755 labfile.txt
 🔹 Change Ownership
    sudo chown devuser labfile.txt
 ✅ Outcome:

Understood Linux permission structure (Owner, Group, Others) and modified file access using chmod and chown.

📸 Screenshot:

# 🧪 Lab 3 – Process Management
  🔹 Run Background Process
     sleep 200 &
  🔹 Check Running Process
     ps aux | grep sleep
  🔹 Kill Process
     kill -9 PID
✅ Outcome:

Learned how to manage running processes, identify PID, and terminate background processes.

📸 Screenshot:

# 🧪 Lab 4 – Vim Text Editor
  🔹 Open File in Vim
     vim labvim.txt
  🔹 Insert Content

    Press:

     i
  🔹 Save & Exit
    :wq
✅ Outcome:

Practiced editing files using Vim editor and understood different modes (Insert, Normal, Command).

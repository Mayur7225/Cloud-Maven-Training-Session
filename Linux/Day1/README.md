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

sudo adduser devuser
###🔹 Switch to the User
```bash
      su - devuser
```
###🔹 Verify Home Directory
```bash
   pwd
```

## 🧪 Lab 2 – File Permissions & Ownership

###  🔹 Create a File
```bash
  touch labfile.txt
```
###🔹 Check Permissions
```bash
  ls -l
```
###🔹 Change Permissions
```bash
  chmod 755 labfile.txt
```
###🔹 Change Ownership
```bash
  sudo chown devuser labfile.txt
```
 ✅ Outcome:

Understood Linux permission structure (Owner, Group, Others) and modified file access using chmod and chown.

📸 Screenshot:

## 🧪 Lab 3 – Process Management

###🔹 Run Background Process
```bash
  sleep 200 &
```
###🔹 Check Running Process
```bash
   ps aux | grep sleep
```
###🔹 Kill Process
```bash
     kill -9 PID
```

✅ Outcome:

Learned how to manage running processes, identify PID, and terminate background processes.

📸 Screenshot:

## 🧪 Lab 4 – Vim Text Editor
###🔹 Open File in Vim
```bash
     vim labvim.txt
```
###🔹 Insert Content
```bash
    Press:
     i
```
###🔹 Save & Exit
```bash   
    :wq
```

✅ Outcome:

Practiced editing files using Vim editor and understood different modes (Insert, Normal, Command).

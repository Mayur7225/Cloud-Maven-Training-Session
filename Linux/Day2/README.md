# 🐧 Linux Day 2 – SSH, Cron, systemd & Log Archiving

## 📌 Overview
This session focused on advanced Linux administration tasks including:

- SSH Key-Based Authentication
- Cron Job Scheduling
- systemd Services & Timers
- Log Archiving using tar

---

# 🧪 Lab 1 – SSH Key Setup

### 🔹 Generate SSH Key
    ```bash
      ssh-keygen
    ```

### 🔹 Copy Key
    ```bash
      ssh-copy-id devuser@localhost
    ```

### 🔹 Disable Password Login

      Edited:
       ```bash
            /etc/ssh/sshd_config
       ```
      Updated:
       ```bash
            PasswordAuthentication no
            PermitRootLogin no
            PubkeyAuthentication yes
       ```
       Restarted:
       ```bash
            sudo systemctl restart ssh
       ```

# 🧪 Lab 2 – Cron Job
  
### 🔹 Create Cron Job
    ```bash
       crontab -e
     ```
  Added:
  ```bash
        * * * * * echo "Test" >> /tmp/test.log
  ```

### 🔹 Verify
    ```bash
         cat /tmp/test.log
    ```

# 🧪 Lab 3 – systemd Timer

### 🔹 Script
      ```bash
         #!/bin/bash
         echo "Hello Systemd" >> /tmp/systemd.log
      ```

### 🔹 Service & Timer Created
 
    Enabled:
           ```bash
              sudo systemctl enable hello.timer
              sudo systemctl start hello.timer
           ```

### 🔹 Verification
       ```bash 
          systemctl list-timers
          cat /tmp/systemd.log
       ```

# 🧪 Homework – Log Archiving

   Created a bash script:
    ```bash
       ./homework-log-archive.sh
    ```
   Script:
    ```bash
       tar -czvf myapp-$(date +%F).tar.gz /var/log/myapp/*.log
    ```

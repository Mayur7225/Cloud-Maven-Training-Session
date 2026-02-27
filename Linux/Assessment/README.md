# Linux Weekly Assessment

## Sections Covered:
- Permissions & umask
- User management
- SSH key setup
- Package management
- Cron job
- Systemd timer
- Networking & tcpdump
- Monitoring & logs
- Bash scripting

## Key Commands Used

### Permissions
touch test.txt
umask
ls -l

### Users
sudo useradd -m -s /bin/bash intern1
sudo chage -E YYYY-MM-DD intern1

### SSH
ssh-keygen
cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
ssh localhost

### Cron
* * * * * /usr/bin/date >> /tmp/cron_test.log

### Monitoring
df -h
du -sh /var/log
ps aux --sort=-%mem | head -4

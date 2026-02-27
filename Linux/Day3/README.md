# Day 3 - Linux Networking & Troubleshooting Lab

## 📌 Objective
In this lab, I learned how networking works in Linux and how to troubleshoot issues step-by-step using real commands.

I understood:
- How a system is identified on a network
- How traffic leaves the machine
- How DNS resolves domain names
- How web traffic works (HTTP)
- How firewall controls incoming connections

---

## 🔹 Task 1 - Verify Network Identity

### Commands Used:
```
   ip addr
   ip route
   hostname -I
```

### What I Learned:
- `ip addr` shows my private IP and network interface.
- `ip route` shows the default gateway (router).
- `hostname -I` quickly displays the system IP.

This helped me understand how my system communicates inside the local network.

---

## 🔹 Task 2 - Test Internet Connectivity Flow

### Commands Used:
```
ping 8.8.8.8
ping google.com
traceroute google.com
```

### Understanding:
- If ping by IP works → Internet is working.
- If IP works but domain fails → DNS issue.
- `traceroute` shows intermediate network hops.

This helped me understand the path packets take to reach the internet.

---

## 🔹 Task 3 - Analyze DNS in Detail

### Commands Used:
```
dig google.com
nslookup google.com
```

### Observed:
- Returned IP addresses
- DNS server used
- Query response time

This demonstrated how domain names resolve to IP addresses.

---

## 🔹 Task 4 - Host a Simple Website Locally

### Installed Nginx:
```
sudo apt install nginx
```

### Created Custom Page:
```
echo "Hello from my server" | sudo tee /var/www/html/index.html
```

### Tested Locally:
curl http://localhost

### Verified Listening Port:
ss-tuln

Port 80 was active, confirming the web server was running.

---

## 🔹 Task 5 - Test Application Layer
curl -I http://localhost

wget http://localhost

Observed HTTP status code `200 OK`, confirming proper server response.

---

## 🔹 Task 6 - Configure Firewall (UFW)

### Enabled Firewall:
sudo ufw enable

### Allowed Only Required Ports:
sudo ufw allow 80
sudo ufw allow 443
sudo ufw allow from <trusted_ip> to any port 22

### Checked Status:
sudo ufw status verbose

This ensured only necessary services were accessible.

---

## 🔹 Key Networking Concepts Learned

- IP Addressing & Routing
- DNS Resolution Process
- TCP Ports & HTTP Flow
- Service Listening Verification
- Firewall Rule Configuration
- Layer-by-layer Troubleshooting Approach

---

## 🔥 Troubleshooting Approach I Followed

1. Check connectivity using `ping`
2. Verify DNS using `dig`
3. Trace route using `traceroute`
4. Check listening ports using `ss`
5. Test application response using `curl`
6. Verify firewall rules using `ufw`

This structured method helps diagnose issues quickly in real-world DevOps environments.

---



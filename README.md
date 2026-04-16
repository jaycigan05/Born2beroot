*This project has been created as part of the 42 curriculum by <yourlogin>.*

# Born2BeRoot

## 📌 Description
Born2BeRoot is a system administration project that introduces the fundamentals of virtualization and Linux server configuration. The objective is to create a secure and minimal virtual machine using VirtualBox, while applying strict security rules such as user management, password policies, firewall configuration, and system monitoring.

This project helps build a strong foundation in Linux system administration and server security.

---

## ⚙️ Instructions

### 1. Virtual Machine Setup
- Software: VirtualBox
- OS: Debian (stable version)
- No graphical interface installed (mandatory)

### 2. System Configuration
- Hostname: `<yourlogin>42`
- Created user: `<yourlogin>`
- Groups:
  - `sudo`
  - `user42`

### 3. Partitioning
- LVM (Logical Volume Manager) enabled
- At least 2 encrypted partitions created

### 4. SSH Configuration
- SSH service installed
- Port set to `4242`
- Root login via SSH disabled

### 5. Firewall (UFW)
- Firewall enabled at startup
- Only port `4242` open

### 6. Password Policy
- Expiry: 30 days
- Minimum days between changes: 2
- Warning: 7 days before expiry
- Requirements:
  - Minimum 10 characters
  - Uppercase, lowercase, number required
  - No more than 3 repeated characters
  - Must not include username
  - Must differ from previous password by 7 characters

### 7. Sudo Configuration
- Maximum 3 authentication attempts
- Custom error message
- Logs stored in `/var/log/sudo/`
- Input/output logging enabled
- TTY mode enabled
- Secure path restricted

### 8. Monitoring Script
- Script name: `monitoring.sh`
- Language: Bash
- Runs every 10 minutes using cron
- Displays:
  - System architecture
  - CPU (physical & virtual)
  - RAM usage
  - Disk usage
  - CPU load
  - Last boot time
  - LVM status
  - TCP connections
  - Logged-in users
  - IP and MAC address
  - Number of sudo commands executed

---

## 🧠 Technical Choices

### 🔹 Operating System: Debian
**Advantages:**
- Stable and secure
- Large community support
- Easy package management (`apt`)

**Disadvantages:**
- Older packages compared to some distributions

---

### 🔹 Debian vs Rocky Linux

| Debian | Rocky Linux |
|--------|------------|
| Uses `apt` | Uses `dnf` |
| Easier for beginners | More enterprise-focused |
| Uses AppArmor | Uses SELinux |

---

### 🔹 AppArmor vs SELinux

| AppArmor | SELinux |
|----------|--------|
| Simpler to configure | More powerful |
| Path-based control | Label-based control |
| Default in Debian | Default in Rocky |

---

### 🔹 UFW vs firewalld

| UFW | firewalld |
|-----|----------|
| Simpler | More advanced |
| Easy for beginners | Used in enterprise |
| Used in Debian | Used in Rocky |

---

### 🔹 VirtualBox vs UTM

| VirtualBox | UTM |
|------------|-----|
| Cross-platform | macOS-focused |
| Widely used | Lightweight alternative |
| More features | Simpler setup |

---

## 📚 Resources

- Debian Documentation: https://www.debian.org/doc/
- Linux Command Reference: https://linuxcommand.org/
- VirtualBox Documentation: https://www.virtualbox.org/wiki/Documentation

### 🤖 AI Usage
AI was used as a learning support tool to:
- Clarify system administration concepts
- Understand Linux commands and configurations
- Debug issues during setup

All configurations and implementations were manually executed and understood.

---

## ✅ Conclusion

This project provided hands-on experience in:
- Linux system administration
- Virtualization
- Security configuration
- Automation using scripts

It builds a strong foundation for future DevOps and system engineering work.

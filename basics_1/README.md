# 🌐 Network Basics 1

## 📋 Overview

This directory contains Bash scripts for network configuration and monitoring tasks as part of the Holberton School Network curriculum. These scripts demonstrate fundamental network operations including DNS configuration, IP address discovery, and port listening.

## 📑 Table of Contents

- [🌐 Network Basics 1](#-network-basics-1)
  - [📋 Overview](#-overview)
  - [📑 Table of Contents](#-table-of-contents)
  - [📁 Repository Information](#-repository-information)
  - [🔧 Scripts](#-scripts)
    - [0️⃣ Change Your Home IP](#️⃣-change-your-home-ip)
      - [📝 Description](#-description)
      - [✅ Requirements](#-requirements)
      - [⚙️ Functionality](#️-functionality)
      - [💻 Usage](#-usage)
      - [📊 Example Output](#-example-output)
      - [⚠️ Important Notes](#️-important-notes)
    - [1️⃣ Show Attached IPs](#️⃣-show-attached-ips)
      - [📝 Description](#-description-1)
      - [⚙️ Functionality](#️-functionality-1)
      - [💻 Usage](#-usage-1)
      - [📊 Example Output](#-example-output-1)
      - [🛠️ Technical Implementation](#️-technical-implementation)
      - [🎯 Use Cases](#-use-cases)
    - [2️⃣ Port Listening on Localhost](#️⃣-port-listening-on-localhost)
      - [📝 Description](#-description-2)
      - [⚙️ Functionality](#️-functionality-2)
      - [💻 Usage](#-usage-2)
      - [🛠️ Technical Implementation](#️-technical-implementation-1)
      - [🧪 Testing the Listener](#-testing-the-listener)
      - [🎯 Use Cases](#-use-cases-1)
  - [📋 Prerequisites](#-prerequisites)
    - [💾 System Requirements](#-system-requirements)
    - [🛠️ Required Tools](#️-required-tools)
      - [🐧 Installation on Ubuntu](#-installation-on-ubuntu)
      - [🍎 Installation on macOS](#-installation-on-macos)
  - [🔐 File Permissions](#-file-permissions)
  - [🛡️ Safety and Best Practices](#️-safety-and-best-practices)
    - [🏠 For `0-change_your_home_IP`](#-for-0-change_your_home_ip)
    - [🌐 For Network Scripts](#-for-network-scripts)
    - [🔒 General Security](#-general-security)
  - [🔧 Troubleshooting](#-troubleshooting)
    - [❓ Common Issues](#-common-issues)
      - [🚫 Script Permission Denied](#-script-permission-denied)
      - [📝 `/etc/hosts` Modification Fails](#--etchosts-modification-fails)
      - [🔍 `ifconfig` Command Not Found](#--ifconfig-command-not-found)
      - [🔌 Port Already in Use](#-port-already-in-use)
      - [🌍 DNS Changes Not Taking Effect](#-dns-changes-not-taking-effect)
  - [🎓 Learning Objectives](#-learning-objectives)
  - [🧪 Testing and Validation](#-testing-and-validation)
    - [🤖 Automated Testing](#-automated-testing)
    - [👨‍💻 Manual Testing](#-manual-testing)
  - [📚 Additional Resources](#-additional-resources)
  - [👨‍💻 Authors](#-authors)
  - [📄 License](#-license)

---

## 📁 Repository Information

- **Repository**: `holbertonschool-network`
- **Directory**: `basics_1`
- **Language**: Bash
- **Environment**: Ubuntu/Linux (with macOS compatibility)

---

## 🔧 Scripts

### 0️⃣ Change Your Home IP
**File**: `0-change_your_home_IP`

#### 📝 Description
A Bash script that configures DNS resolution by modifying the `/etc/hosts` file to customize how specific domains resolve locally.

#### ✅ Requirements
- `localhost` must resolve to `127.0.0.2`
- `facebook.com` must resolve to `8.8.8.8`

#### ⚙️ Functionality
1. **Backup Creation**: Creates a backup of the original `/etc/hosts` file as `/etc/hosts.backup`
2. **Entry Removal**: Removes any existing entries for `localhost` and `facebook.com`
3. **Custom Resolution**: Adds new DNS resolution entries
4. **Safe Implementation**: Uses temporary files to ensure atomic updates

#### 💻 Usage
```bash
sudo ./0-change_your_home_IP
```

#### 📊 Example Output
**Before running the script:**
```bash
$ ping localhost
PING localhost (127.0.0.1) 56(84) bytes of data.
64 bytes from localhost (127.0.0.1): icmp_seq=1 ttl=64 time=0.012 ms

$ ping facebook.com
PING facebook.com (157.240.11.35) 56(84) bytes of data.
64 bytes from edge-star-mini-shv-02-lax3.facebook.com (157.240.11.35): icmp_seq=1 ttl=63 time=15.4 ms
```

**After running the script:**
```bash
$ ping localhost
PING localhost (127.0.0.2) 56(84) bytes of data.
64 bytes from localhost (127.0.0.2): icmp_seq=1 ttl=64 time=0.012 ms

$ ping facebook.com
PING facebook.com (8.8.8.8) 56(84) bytes of data.
64 bytes from facebook.com (8.8.8.8): icmp_seq=1 ttl=63 time=8.06 ms
```

#### ⚠️ Important Notes
- **Requires root privileges**: Must be run with `sudo`
- **System Impact**: Modifies system-level DNS resolution
- **Revert Instructions**: To restore original settings, run `sudo cp /etc/hosts.backup /etc/hosts`
- **Production Warning**: Only use on development/test machines

---

### 1️⃣ Show Attached IPs
**File**: `1-show_attached_IPs`

#### Description
A Bash script that displays all active IPv4 IP addresses currently attached to the machine's network interfaces.

#### Functionality
- Extracts IPv4 addresses from `ifconfig` output
- Uses portable regex patterns for cross-platform compatibility
- Displays one IP address per line

#### Usage
```bash
./1-show_attached_IPs
```

#### Example Output
```
127.0.0.1
192.168.1.14
192.168.2.1
10.0.0.15
```

#### 🛠️ Technical Implementation
```bash
ifconfig | grep -oE 'inet ([0-9]{1,3}\.){3}[0-9]{1,3}' | cut -d' ' -f2
```

#### 🎯 Use Cases
- Network troubleshooting
- System inventory
- Configuration verification
- Security auditing

---

### 2️⃣ Port Listening on Localhost
**File**: `2-port_listening_on_localhost`

#### Description
A Bash script that creates a network listener on localhost port 98 using netcat.

#### Functionality
- Binds to localhost (`127.0.0.1`) on port 98
- Creates a TCP listener that accepts incoming connections
- Useful for testing network connectivity and port availability

#### Usage
```bash
./2-port_listening_on_localhost
```

#### Technical Implementation
```bash
nc -l 127.0.0.1 98
```

#### 🧪 Testing the Listener
From another terminal:
```bash
# Test connection
telnet localhost 98
# or
nc localhost 98

# Verify port is listening
netstat -tlnp | grep :98
# or
ss -tlnp | grep :98
```

#### Use Cases
- Network service testing
- Port availability verification
- TCP connection troubleshooting
- Learning network fundamentals

---

## 📋 Prerequisites

### 💾 System Requirements
- **Operating System**: Ubuntu/Linux (primary), macOS (compatible)
- **Shell**: Bash
- **Privileges**: Root access required for scripts modifying system files

### 🛠️ Required Tools
Ensure the following tools are installed:
- `ifconfig` (part of net-tools package)
- `netcat` (`nc` command)
- `grep`, `cut`, `cp` (standard Unix tools)

#### 🐧 Installation on Ubuntu
```bash
sudo apt update
sudo apt install net-tools netcat-openbsd
```

#### 🍎 Installation on macOS
```bash
# ifconfig is pre-installed
# netcat is pre-installed as nc
brew install grep  # for GNU grep if needed
```

---

## 🔐 File Permissions

All scripts should be executable:
```bash
chmod +x 0-change_your_home_IP
chmod +x 1-show_attached_IPs
chmod +x 2-port_listening_on_localhost
```

---

## 🛡️ Safety and Best Practices

### 🏠 For `0-change_your_home_IP`
1. **Always backup**: The script creates `/etc/hosts.backup` automatically
2. **Test environment**: Only use on development/test machines
3. **Revert changes**: Remember to restore original settings after testing
4. **Monitor impact**: Some applications may behave differently with modified DNS

### 🌐 For Network Scripts
1. **Port conflicts**: Ensure port 98 is not already in use before running the listener
2. **Firewall settings**: Check firewall rules if connections fail
3. **Process cleanup**: Remember to stop listening processes when done

### 🔒 General Security
1. **Privilege escalation**: Only run with elevated privileges when necessary
2. **Code review**: Always review scripts before execution
3. **Environment isolation**: Test in isolated environments first

---

## 🔧 Troubleshooting

### ❓ Common Issues

#### 🚫 Script Permission Denied
```bash
# Make scripts executable
chmod +x script_name
```

#### 📝 `/etc/hosts` Modification Fails
```bash
# Ensure running with sudo
sudo ./0-change_your_home_IP
```

#### 🔍 `ifconfig` Command Not Found
```bash
# Ubuntu/Debian
sudo apt install net-tools

# Alternative: use ip command
ip addr show
```

#### 🔌 Port Already in Use
```bash
# Check what's using the port
sudo netstat -tlnp | grep :98
sudo ss -tlnp | grep :98

# Kill process using the port (replace PID)
kill PID
```

#### 🌍 DNS Changes Not Taking Effect
```bash
# Flush DNS cache (Ubuntu)
sudo systemctl restart systemd-resolved

# Flush DNS cache (macOS)
sudo dscacheutil -flushcache
sudo killall -HUP mDNSResponder

# Verify resolution
getent hosts localhost
getent hosts facebook.com
```

---

## 🎓 Learning Objectives

After completing these exercises, you should understand:

1. **DNS Resolution**: How `/etc/hosts` affects domain name resolution
2. **Network Interfaces**: How to discover and list IP addresses on a system
3. **Port Binding**: How to create network listeners and test connectivity
4. **System Administration**: Safe practices for modifying system files
5. **Network Troubleshooting**: Tools and techniques for diagnosing network issues

---

## 🧪 Testing and Validation

### 🤖 Automated Testing
These scripts are designed to pass automated testing systems that verify:
- Correct DNS resolution changes
- Proper IP address extraction
- Successful port binding

### 👨‍💻 Manual Testing
```bash
# Test DNS changes
./0-change_your_home_IP
getent hosts localhost  # Should show 127.0.0.2
getent hosts facebook.com  # Should show 8.8.8.8

# Test IP discovery
./1-show_attached_IPs > ips.txt
cat ips.txt  # Verify output format

# Test port listener
./2-port_listening_on_localhost &
netstat -tlnp | grep :98  # Should show listening port
kill %1  # Stop background listener
```

---

## 📚 Additional Resources

- [Linux Network Commands Cheat Sheet](https://www.cyberciti.biz/faq/linux-unix-networking-commands/)
- [Understanding /etc/hosts File](https://www.howtogeek.com/howto/27350/beginner-geek-how-to-edit-your-hosts-file/)
- [Netcat (nc) Command Examples](https://www.cyberciti.biz/faq/linux-port-scanning/)
- [Network Troubleshooting Guide](https://www.redhat.com/sysadmin/beginners-guide-network-troubleshooting-linux)

---

## 👨‍💻 Authors

- **Héctor Soto** - [@hector17rock](https://github.com/hector17rock)
- **Holberton School** - Network Curriculum

---

## 📄 License

This project is part of the Holberton School curriculum.

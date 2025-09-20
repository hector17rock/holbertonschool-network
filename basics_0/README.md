# 🌐 Network Basics 0

## 📋 Overview

This directory contains foundational network exercises covering essential networking concepts. These exercises test theoretical knowledge about networking protocols, models, and practical skills with network troubleshooting tools. This is the first module in the Holberton School Network curriculum, focusing on fundamental concepts that form the backbone of modern networking.

## 📑 Table of Contents

- [🌐 Network Basics 0](#-network-basics-0)
  - [📋 Overview](#-overview)
  - [📑 Table of Contents](#-table-of-contents)
  - [📁 Repository Information](#-repository-information)
  - [📚 Exercises](#-exercises)
    - [0️⃣ OSI Model](#️⃣-osi-model)
      - [📝 Description](#-description)
      - [🎯 Learning Objectives](#-learning-objectives)
      - [💡 Answer](#-answer)
      - [📖 Explanation](#-explanation)
    - [1️⃣ Types of Network](#️⃣-types-of-network)
      - [📝 Description](#-description-1)
      - [🎯 Learning Objectives](#-learning-objectives-1)
      - [💡 Answers](#-answers)
      - [📖 Explanation](#-explanation-1)
    - [2️⃣ MAC and IP Address](#️⃣-mac-and-ip-address)
      - [📝 Description](#-description-2)
      - [🎯 Learning Objectives](#-learning-objectives-2)
      - [💡 Answers](#-answers-1)
      - [📖 Explanation](#-explanation-2)
    - [3️⃣ UDP and TCP](#️⃣-udp-and-tcp)
      - [📝 Description](#-description-3)
      - [🎯 Learning Objectives](#-learning-objectives-3)
      - [💡 Answers](#-answers-2)
      - [📖 Explanation](#-explanation-3)
    - [4️⃣ TCP and UDP Ports](#️⃣-tcp-and-udp-ports)
      - [📝 Description](#-description-4)
      - [🎯 Learning Objectives](#-learning-objectives-4)
      - [💻 Usage](#-usage)
      - [📊 Example Output](#-example-output)
      - [🛠️ Technical Implementation](#️-technical-implementation)
    - [5️⃣ Is the Host on the Network](#️⃣-is-the-host-on-the-network)
      - [📝 Description](#-description-5)
      - [🎯 Learning Objectives](#-learning-objectives-5)
      - [💻 Usage](#-usage-1)
      - [📊 Example Output](#-example-output-1)
      - [🛠️ Technical Implementation](#️-technical-implementation-1)
  - [📋 Prerequisites](#-prerequisites)
    - [💾 System Requirements](#-system-requirements)
    - [🛠️ Required Tools](#️-required-tools)
      - [🐧 Installation on Ubuntu](#-installation-on-ubuntu)
      - [🍎 Installation on macOS](#-installation-on-macos)
  - [🔐 File Permissions](#-file-permissions)
  - [🎓 Learning Objectives](#-learning-objectives-6)
  - [🧪 Testing and Validation](#-testing-and-validation)
    - [🤖 Automated Testing](#-automated-testing)
    - [👨‍💻 Manual Testing](#-manual-testing)
  - [🛡️ Best Practices](#️-best-practices)
  - [🔧 Troubleshooting](#-troubleshooting)
  - [📚 Additional Resources](#-additional-resources)
  - [👨‍💻 Authors](#-authors)
  - [📄 License](#-license)

---

## 📁 Repository Information

- **Repository**: `holbertonschool-network`
- **Directory**: `basics_0`
- **Language**: Bash (for scripts), Text (for answers)
- **Environment**: Ubuntu/Linux (with macOS compatibility)
- **Course**: Holberton School Network Fundamentals

---

## 📚 Exercises

### 0️⃣ OSI Model
**File**: `0-OSI_model`

#### 📝 Description
This exercise tests understanding of the OSI (Open Systems Interconnection) model, specifically focusing on how it's organized and what the Transport layer does.

**Questions:**
1. What is the OSI model?
   - Set of specifications that network hardware manufacturers must respect
   - **The OSI model is a conceptual model that characterizes the communication functions of a telecommunication system without regard to their underlying internal structure and technology**
   - The OSI model is a model that characterizes the communication functions of a telecommunication system with a strong regard for their underlying internal structure and technology

2. How is the OSI model organized?
   - Alphabetically
   - **From the lowest to the highest level**
   - Randomly

#### 🎯 Learning Objectives
- Understand the OSI model's purpose and structure
- Learn about the seven layers of the OSI model
- Comprehend the hierarchical organization from Physical to Application layer

#### 💡 Answer
```
2
2
```

#### 📖 Explanation
- **Answer 1 (2)**: The OSI model is a conceptual framework that standardizes communication functions
- **Answer 2 (2)**: The OSI model is organized from the lowest level (Physical Layer 1) to the highest level (Application Layer 7)

**The 7 OSI Layers:**
1. 🔌 **Physical Layer** - Hardware transmission of raw bits
2. 🔗 **Data Link Layer** - Node-to-node data transfer
3. 🛣️ **Network Layer** - Routing and IP addressing
4. 🚚 **Transport Layer** - End-to-end data delivery (TCP/UDP)
5. 💻 **Session Layer** - Session management
6. 🎨 **Presentation Layer** - Data formatting and encryption
7. 📱 **Application Layer** - Network services to applications

---

### 1️⃣ Types of Network
**File**: `1-types_of_network`

#### 📝 Description
This exercise covers different types of networks and their typical connection scenarios, focusing on LAN, WAN, and Internet classifications.

**Questions:**
1. What type of network a computer in local is connected to?
   - Internet
   - WAN
   - **LAN**

2. What type of network could connect an office in one building to another office in a building a few streets away?
   - Internet
   - **WAN**
   - LAN

3. What network do you use when you browse www.google.com from your smartphone (not connected to the Wifi)?
   - **Internet**
   - WAN
   - LAN

#### 🎯 Learning Objectives
- Distinguish between LAN, WAN, and Internet networks
- Understand network scope and geographical coverage
- Learn real-world network classification scenarios

#### 💡 Answers
```
3
2
1
```

#### 📖 Explanation
- **Answer 1 (3 - LAN)**: Local Area Network connects devices in a single location
- **Answer 2 (2 - WAN)**: Wide Area Network connects geographically separated locations
- **Answer 3 (1 - Internet)**: Global network accessed via cellular data

**Network Types Overview:**
- 🏠 **LAN (Local Area Network)**: Small geographical area (home, office, building)
- 🌆 **WAN (Wide Area Network)**: Large geographical area (cities, countries)
- 🌍 **Internet**: Global network of interconnected networks

---

### 2️⃣ MAC and IP Address
**File**: `2-MAC_and_IP_address`

#### 📝 Description
This exercise tests knowledge about MAC addresses and IP addresses, their purposes, and characteristics.

**Questions:**
1. What is a MAC address?
   - The name of a network interface
   - **The unique identifier of a network interface**
   - A network interface

2. What is an IP address?
   - **Is to devices connected to a network what postal address is to houses**
   - The unique identifier of a network interface
   - A network interface

#### 🎯 Learning Objectives
- Understand the difference between MAC and IP addresses
- Learn the purpose and scope of each addressing system
- Comprehend addressing in network communication

#### 💡 Answers
```
2
1
```

#### 📖 Explanation
- **Answer 1 (2)**: MAC address is the unique hardware identifier of a network interface
- **Answer 2 (1)**: IP address serves as a logical address for network routing, like a postal address

**Address Comparison:**
- 🔧 **MAC Address**: 
  - Hardware-based, permanent identifier
  - 6 bytes (48 bits), e.g., `00:1B:44:11:3A:B7`
  - Used at Data Link Layer (Layer 2)
  - Local network scope

- 📮 **IP Address**: 
  - Logical, changeable identifier
  - IPv4: 4 bytes (32 bits), e.g., `192.168.1.1`
  - Used at Network Layer (Layer 3)
  - Global routing scope

---

### 3️⃣ UDP and TCP
**File**: `3-UDP_and_TCP`

#### 📝 Description
This exercise focuses on understanding the characteristics and use cases of UDP and TCP protocols at the Transport Layer.

**Questions:**
1. Which statement is correct for the TCP box:
   - **It is a protocol that is transferring data in a reliable way**
   - It is a protocol that is transferring data in a fast way
   - It is a protocol that is transferring data in an unreliable way

2. Which statement is correct for the UDP box:
   - It is a protocol that is transferring data in a reliable way
   - **It is a protocol that is transferring data in a fast way**
   - It is a protocol that is transferring data in an unreliable way

3. Which statement is correct for the TCP worker:
   - **Have you received boxes x, y, z?**
   - Sending boxes x, y, z
   - Have you received box x?

#### 🎯 Learning Objectives
- Understand TCP vs UDP characteristics
- Learn about reliable vs unreliable data transfer
- Comprehend the trade-offs between reliability and speed

#### 💡 Answers
```
1
2
1
```

#### 📖 Explanation
- **Answer 1 (1)**: TCP provides reliable, connection-oriented data transfer
- **Answer 2 (2)**: UDP prioritizes speed over reliability (connectionless)
- **Answer 3 (1)**: TCP confirms receipt of data packets (acknowledgment mechanism)

**Protocol Comparison:**
- 🛡️ **TCP (Transmission Control Protocol)**:
  - Reliable, connection-oriented
  - Error checking and correction
  - Slower but guaranteed delivery
  - Used for: HTTP, HTTPS, FTP, email

- ⚡ **UDP (User Datagram Protocol)**:
  - Fast, connectionless
  - No error correction
  - Faster but no delivery guarantee
  - Used for: DNS, video streaming, gaming

---

### 4️⃣ TCP and UDP Ports
**File**: `4-TCP_and_UDP_ports`

#### 📝 Description
A Bash script that displays all listening ports on the system, showing both the port numbers and the associated processes.

#### 🎯 Learning Objectives
- Learn to monitor network ports and services
- Understand the relationship between ports and processes
- Practice network troubleshooting techniques

#### 💻 Usage
```bash
./4-TCP_and_UDP_ports
```

#### 📊 Example Output
```
Active Internet connections (only servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State       PID/Program name    
tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN      1234/sshd           
tcp        0      0 127.0.0.1:631           0.0.0.0:*               LISTEN      5678/cupsd          
tcp6       0      0 :::80                   :::*                    LISTEN      9101/apache2        
udp        0      0 0.0.0.0:68              0.0.0.0:*                           1121/dhclient       
```

#### 🛠️ Technical Implementation
```bash
#!/usr/bin/env bash
# Script that displays listening ports with PID and program names

netstat -lp
```

**Command Options:**
- `-l`: Show only listening ports
- `-p`: Show PID and program name

---

### 5️⃣ Is the Host on the Network
**File**: `5-is_the_host_on_the_network`

#### 📝 Description
A Bash script that pings an IP address to check if a host is reachable on the network. The script accepts an IP address as an argument and sends 5 ping packets.

#### 🎯 Learning Objectives
- Learn network connectivity testing
- Understand ping command and ICMP protocol
- Practice script argument handling and validation

#### 💻 Usage
```bash
./5-is_the_host_on_the_network {IP_ADDRESS}
```

#### 📊 Example Output
**Successful ping:**
```bash
$ ./5-is_the_host_on_the_network 8.8.8.8
PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=118 time=12.3 ms
64 bytes from 8.8.8.8: icmp_seq=2 ttl=118 time=11.8 ms
64 bytes from 8.8.8.8: icmp_seq=3 ttl=118 time=12.1 ms
64 bytes from 8.8.8.8: icmp_seq=4 ttl=118 time=11.9 ms
64 bytes from 8.8.8.8: icmp_seq=5 ttl=118 time=12.0 ms

--- 8.8.8.8 ping statistics ---
5 packets transmitted, 5 received, 0% packet loss, time 4006ms
rtt min/avg/max/mdev = 11.836/12.032/12.301/0.172 ms
```

**No argument provided:**
```bash
$ ./5-is_the_host_on_the_network
Usage: 5-is_the_host_on_the_network {IP_ADDRESS}
```

#### 🛠️ Technical Implementation
```bash
#!/usr/bin/env bash
# Script that pings an IP address passed as an argument

if [ $# -eq 0 ]; then
    echo "Usage: 5-is_the_host_on_the_network {IP_ADDRESS}"
    exit 1
fi

ping -c 5 "$1"
```

**Script Features:**
- Argument validation
- 5 ping attempts (`-c 5`)
- Proper usage message
- Safe argument handling with quotes

---

## 📋 Prerequisites

### 💾 System Requirements
- **Operating System**: Ubuntu/Linux (primary), macOS (compatible)
- **Shell**: Bash
- **Network**: Internet connection for testing

### 🛠️ Required Tools
Ensure the following tools are installed:
- `netstat` (part of net-tools package)
- `ping` (usually pre-installed)
- `bash` (shell interpreter)

#### 🐧 Installation on Ubuntu
```bash
sudo apt update
sudo apt install net-tools
```

#### 🍎 Installation on macOS
```bash
# ping and netstat are pre-installed
# If you need GNU versions:
brew install gnu-netcat
```

---

## 🔐 File Permissions

Executable scripts should have proper permissions:
```bash
chmod +x 4-TCP_and_UDP_ports
chmod +x 5-is_the_host_on_the_network
```

---

## 🎓 Learning Objectives

After completing these exercises, you should understand:

1. **OSI Model**: The seven-layer networking model and its organization
2. **Network Types**: Differences between LAN, WAN, and Internet
3. **Addressing**: MAC vs IP addresses and their purposes
4. **Transport Protocols**: TCP vs UDP characteristics and use cases
5. **Network Monitoring**: How to check listening ports and services
6. **Connectivity Testing**: Using ping to test network reachability
7. **Bash Scripting**: Creating network diagnostic scripts

---

## 🧪 Testing and Validation

### 🤖 Automated Testing
These exercises are designed for automated grading systems that check:
- Correct answers in text files
- Script functionality and output format
- Proper error handling

### 👨‍💻 Manual Testing

**Test theoretical knowledge:**
```bash
# Check answer files
cat 0-OSI_model        # Should show: 2\n2
cat 1-types_of_network # Should show: 3\n2\n1
cat 2-MAC_and_IP_address # Should show: 2\n1
cat 3-UDP_and_TCP      # Should show: 1\n2\n1
```

**Test scripts:**
```bash
# Test port listing
./4-TCP_and_UDP_ports | head -10

# Test ping script
./5-is_the_host_on_the_network 8.8.8.8
./5-is_the_host_on_the_network  # Should show usage message
```

---

## 🛡️ Best Practices

### 📚 For Theory Questions
1. **Understand concepts**: Don't just memorize answers
2. **Practice examples**: Apply concepts to real scenarios
3. **Review fundamentals**: Ensure solid foundation knowledge

### 💻 For Scripts
1. **Test thoroughly**: Verify scripts work with different inputs
2. **Handle errors**: Always validate user input
3. **Document code**: Add clear comments explaining functionality
4. **Security**: Be cautious when running network diagnostic tools

---

## 🔧 Troubleshooting

### ❓ Common Issues

#### 🚫 Script Permission Denied
```bash
# Make scripts executable
chmod +x 4-TCP_and_UDP_ports
chmod +x 5-is_the_host_on_the_network
```

#### 🔍 `netstat` Command Not Found
```bash
# Ubuntu/Debian
sudo apt install net-tools

# Alternative: use ss command
ss -tlnp  # Similar to netstat -lp
```

#### 🌐 Ping Permission Issues
```bash
# If ping fails with permission errors
sudo ./5-is_the_host_on_the_network 8.8.8.8
```

#### 📝 Wrong Answer Format
- Ensure answer files contain only the numbers
- Check for extra spaces or characters
- Verify line endings are correct

---

## 📚 Additional Resources

- [OSI Model Explained](https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/)
- [TCP vs UDP Explained](https://www.geeksforgeeks.org/differences-between-tcp-and-udp/)
- [Network Types (LAN, WAN, Internet)](https://www.cisco.com/c/en/us/solutions/small-business/resource-center/networking/network-types.html)
- [MAC vs IP Addresses](https://www.guru99.com/difference-between-mac-and-ip-address.html)
- [Linux Network Commands](https://www.cyberciti.biz/faq/linux-unix-networking-commands/)
- [Ping Command Tutorial](https://linuxize.com/post/linux-ping-command/)

---

## 👨‍💻 Authors

- **Héctor Soto** - [@hector17rock](https://github.com/hector17rock)
- **Holberton School** - Network Curriculum

---

## 📄 License

This project is part of the Holberton School curriculum.

# 🌐 Holberton School Network

![Linux](https://img.shields.io/badge/Linux-Networking-orange.svg)
![Bash](https://img.shields.io/badge/Bash-Scripting-green.svg)
![Progress](https://img.shields.io/badge/Progress-Intermediate-yellow.svg)

## 📖 Description
This repository contains scripts and projects related to networking concepts and protocols as part of the Holberton School curriculum. The projects cover fundamental networking concepts, configurations, and troubleshooting techniques essential for understanding how computer networks function and communicate. These exercises provide hands-on experience with network tools and protocols in Linux environments.

The topics covered include:
- OSI model and TCP/IP architecture
- Network interfaces and IP addressing
- Subnet masks and network segmentation
- DNS resolution and hostname configuration
- Common networking protocols (HTTP, HTTPS, FTP, SSH)
- Firewall configuration and network security
- Network troubleshooting and diagnostic tools

## 📂 Contents
- **basics_0/**: First projects covering network fundamentals:
  - **0-OSI_model**: Understanding the OSI model layers.
  - **1-types_of_network**: Different types of networks and their characteristics.
  - **2-MAC_and_IP_address**: Understanding MAC and IP addressing.
  - **3-UDP_and_TCP**: Comparison of UDP and TCP protocols.
  - **4-TCP_and_UDP_ports**: Working with network ports and services.
  - **5-is_the_host_on_the_network**: Ping utility and connectivity testing.
- **basics_1/**: Contains scripts for network configuration and monitoring:
  - **0-change_your_home_IP**: Configures an Ubuntu server with the following requirements:
    - localhost resolves to 127.0.0.2
    - facebook.com resolves to 8.8.8.8
  - **1-show_attached_IPs**: Displays all active IPv4 IPs on the machine it's executed on.
  - **2-port_listening_on_localhost**: A script that listens on port 98 on localhost.

## 🚀 Getting Started
1. Clone the repository to access the materials:
   ```bash
   git clone https://github.com/jbn179/holbertonschool-network.git
   ```
2. Navigate to the directory:
   ```bash
   cd holbertonschool-network
   ```
3. Run the Bash scripts (make sure they are executable):
   ```bash
   chmod +x basics_0/5-is_the_host_on_the_network
   ./basics_0/5-is_the_host_on_the_network 8.8.8.8
   ```

## 🛠️ Requirements
- Linux operating system (Ubuntu 20.04 LTS recommended)
- Basic knowledge of Bash scripting
- Network tools such as ifconfig, ping, netstat, traceroute

## Examples

### Using ping to check network connectivity
```bash
#!/usr/bin/env bash
# Script to check if a host is reachable

if [ $# -eq 0 ]; then
    echo "Usage: 5-is_the_host_on_the_network {IP_ADDRESS}"
    exit 1
fi

ping -c 5 "$1"
```

### Displaying network interfaces
```bash
#!/usr/bin/env bash
# Script to display network interfaces

ifconfig -a
```

### Checking open ports
```bash
#!/usr/bin/env bash
# Script to list open TCP ports

netstat -tuln
```

## Network Concepts Explained

### OSI Model
The OSI (Open Systems Interconnection) model is a conceptual framework that standardizes the functions of a telecommunication or computing system into seven abstraction layers:
1. Physical Layer
2. Data Link Layer
3. Network Layer
4. Transport Layer
5. Session Layer
6. Presentation Layer
7. Application Layer

### TCP vs UDP
TCP (Transmission Control Protocol):
- Connection-oriented protocol
- Reliable data delivery
- Flow control and congestion management
- Used for applications requiring high reliability

UDP (User Datagram Protocol):
- Connectionless protocol
- No guarantee of delivery
- No flow control or congestion control
- Faster for applications where speed is prioritized over reliability

### IP Addressing
IP addresses are unique identifiers assigned to devices on a network:
- IPv4: 32-bit address (e.g., 192.168.1.1)
- IPv6: 128-bit address (e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334)
- Subnet masks determine which portion of an IP address refers to the network and which refers to hosts

## License
![License](https://img.shields.io/badge/License-MIT-green.svg)  
This project is under the MIT License.

## Author
Benjamin Ristord - [@jbn179](https://github.com/jbn179)
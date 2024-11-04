# Network-Scanner-and-Fingerprinting-Tool

## Overview
This project is a Python-based network scanning tool designed to detect devices within a network, identify open ports, and perform OS and service fingerprinting. The tool leverages the power of Python along with libraries like Scapy and Nmap to gather detailed information about networked devices and the services running on them.

## Features
- **Network Scanning**: Identifies all active devices on the network.
- **Port Scanning**: Detects open ports on each device to understand accessible services.
- **OS Fingerprinting**: Determines the operating system of each device.
- **Service Fingerprinting**: Identifies the services running on detected open ports.

## Technologies Used
- **Python**: The primary programming language used for building the tool.
- **Scapy**: A Python library used for low-level network operations and packet manipulation.
- **Nmap**: An open-source network scanner integrated into the tool to perform OS and service fingerprinting.
- **Linux OS**: Developed and tested in a Linux environment, though it may work on other OSes with Python and Nmap installed.

## Prerequisites
- **Python 3.x** installed on your system.
- **Scapy** library (install via `pip install scapy`).
- **Nmap** installed (installable on Linux via `sudo apt install nmap`).
- Administrative (root) privileges to allow network interface access.

## Installation
Clone this repository:
```bash
git clone https://github.com/your-username/network-scanning-tool.git
cd network-scanning-tool
```

Install the required Python packages:
```bash
pip install -r requirements.txt
```

Make sure Nmap is installed:
```bash
pip install nmap
```

## Usage
Run the tool with Python:
```bash
python network_scanner.py
```

You may need to provide specific flags or inputs, depending on your use case. For example:
- Specify the IP range or subnet to scan.
- Choose options for detailed scans (e.g., for OS or service fingerprinting).

### Example
```bash
python network_scanner.py --network 192.168.1.0/24
```

This command will:
1. Scan all devices within the `192.168.1.0/24` network range.
2. Detect open ports and services.
3. Perform OS and service fingerprinting.
4. Save results in a CSV file for later analysis.

### CSV Output
The scan results will be saved in a CSV file (`scan_results.csv`), containing information such as:
- **IP Address**
- **Open Ports**
- **Detected OS**
- **Detected Services**

## Notes
- **Root privileges** are required to access network interfaces and send/receive network packets.
- Running the tool in large networks may take some time depending on network size and scan depth.
- Ensure you have permission to scan the network; unauthorized scanning is illegal and against ethical hacking principles.


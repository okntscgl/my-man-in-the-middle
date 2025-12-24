# Man-in-the-Middle (MitM) Attack Scripts

This repository contains two Python scripts demonstrating **Man-in-the-Middle (MitM)** attack techniques using the **Scapy** library.  
The project focuses on understanding how ARP poisoning works and how unencrypted network traffic can be intercepted and analyzed.

> ⚠️ **Legal & Ethical Warning**  
> These scripts are provided **strictly for educational, research, and defensive security purposes**.  
> Running MitM attacks on networks or systems without **explicit authorization** is illegal and unethical.  
> Use this project only in lab environments, penetration testing training, or systems you own.

---

## Table of Contents

- [Overview](#overview)
- [Scripts Included](#scripts-included)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Security Notes](#security-notes)
- [License](#license)

---

## Overview

A Man-in-the-Middle (MitM) attack allows an attacker to intercept and potentially manipulate communication between two parties without their knowledge.

This repository demonstrates:
- ARP poisoning to redirect traffic
- Packet sniffing to analyze HTTP traffic
- Practical risks of unencrypted network communication

The goal is to **understand the attack surface** in order to improve detection and prevention strategies.

---

## Scripts Included

### 1. ARP Poisoning Script (`arp_poisoning.py`)

- Performs ARP spoofing between a target machine and the gateway
- Redirects network traffic through the attacker's machine
- Maintains the poisoned ARP cache during execution

### 2. Packet Sniffer Script (`packet_sniffer.py`)

- Listens to network traffic using Scapy
- Captures and analyzes HTTP packets
- Demonstrates how sensitive data can be exposed over unencrypted protocols

---

## Requirements

- Python 3.x
- Scapy
- Scapy-HTTP (optional, used for HTTP packet parsing)

---

## Installation

Install the required dependencies using pip:

```bash
pip install scapy scapy-http
Ensure you run the scripts with sufficient privileges (e.g., root or administrator), as raw packet manipulation is required.

Usage
ARP Poisoning
Run the ARP poisoning script by specifying the target IP and the gateway IP:

bash
python arp_poisoning.py -t <TARGET_IP> -g <GATEWAY_IP>
Example:

bash
python arp_poisoning.py -t 192.168.1.10 -g 192.168.1.1
Packet Sniffing
Start the packet sniffer to monitor and analyze HTTP traffic:

bash
python packet_sniffer.py
Note: This script is effective primarily on unencrypted (HTTP) traffic.
HTTPS traffic cannot be read without additional techniques and certificates.

Project Structure
bash
.
├── arp_poisoning.py     # ARP spoofing / poisoning script
├── packet_sniffer.py   # Network packet sniffer
├── README.md           # Project documentation
Security Notes
This project intentionally demonstrates insecure scenarios for learning purposes.

In real-world environments:

Use HTTPS everywhere

Enable ARP inspection and DHCP snooping

Monitor ARP anomalies

Apply network segmentation

Educate users about unsecured networks

Understanding MitM techniques is essential for defensive security, SOC analysis, and network hardening.

License
This project is licensed under the MIT License.
You are free to use, modify, and distribute this code for educational and ethical purposes only.

# Man-in-the-Middle (MitM) Attack Scripts

This repository contains two Python scripts that implement Man-in-the-Middle (MitM) attacks using the Scapy library. The first script performs ARP poisoning to redirect traffic between a target device and a gateway, while the second script listens for and analyzes HTTP packets.

## Requirements

- Python 3.x
- Scapy
- Scapy-HTTP (optional, for HTTP packet analysis)

Usage
Run the script using the following command:

bash

python arp_poisoning.py -t <TARGET_IP> -g <GATEWAY_IP>

Usage
Run the script using the following command:

bash

python packet_sniffer.py

You can install the required libraries using pip:

```bash
pip install scapy scapy-http

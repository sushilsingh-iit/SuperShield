
🛡️ SuperShield: Custom Personal Firewall

Author - Sushil Singh

A high-performance, real-time personal firewall built from scratch in Python.

Final Capstone Project • Indian Institute of Technology (IIT) Patna • May 2026

📖 About The Project

In today's digital environment, cyber threats such as unauthorized access, malware attacks, and network intrusions are increasingly common. SuperShield is a lightweight, custom personal firewall designed to monitor, analyze, and filter network traffic in real-time.

Developed as a Capstone Project for the Hybrid UG Program in Computer Science & Data Analytics at IIT Patna, this firewall bridges the gap between theoretical networking concepts and real-world cybersecurity implementation.

✨ Core Features

Live Packet Sniffing: Captures network packets in real-time using Scapy. Extracts IPs, protocols, and payloads.

IP & CIDR Blocking: Persistent blocklist of individual IPs and ranges. Suspicious packets are dropped instantly.

Custom Rule Engine: Modular rule system supporting per-protocol (TCP/UDP/ICMP) and per-port filtering logic.

Dual Interface: Run via a powerful, interactive CLI or a full desktop GUI built with Tkinter.

Structured Logging: Comprehensive CSV/Log files detailing timestamps, protocols, and actions taken for security auditing.

⚙️ System Architecture

The firewall is divided into five core modules with a single responsibility, wired together to create a cohesive security layer:

Packet Sniffer: Runs on a background thread, parsing incoming IP, TCP, and UDP headers seamlessly.

Rules Engine: Evaluates extracted headers against a JSON-loaded configuration and IP blocklist in real-time.

Action Handler: Determines whether to silently drop the packet or allow it to proceed to the OS networking stack.

Activity Logger: Writes structured allow/block decisions to firewall logs using Python's native logging framework.

Interface (GUI/CLI): Pulls metrics from the monitor module to update the Tkinter dashboard or terminal UI.

🚀 Quick Installation

To get SuperShield running on your local machine, follow these steps.
(Note: Requires Python 3.9+ and root/admin privileges for raw network interface access).

# 1. Clone the repository
git clone [https://github.com/sushilsingh-iit/SuperShield.git](https://github.com/sushilsingh-iit/SuperShield.git)

# 2. Navigate to the project directory
cd SuperShield

# 3. Create a virtual environment and activate it
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

# 4. Install required dependencies
pip install -r requirements.txt

# 5. Launch the firewall (GUI Mode)
sudo python main.py gui


💻 CLI Usage Examples

For power users and server environments, SuperShield comes with a robust Command Line Interface:

# Start live monitoring dashboard in the terminal
sudo python main.py sniff --dashboard

# Block a specific IP address
sudo python main.py block 203.0.113.50

# Block a specific domain
sudo python main.py block-site facebook.com

# List all currently blocked rules
python main.py list-blocked


🔮 Future Scope / Roadmap

Phase 1 & 2: Core Firewall Engine & Desktop GUI (Completed)

Phase 3: Machine Learning Integration for Anomaly Detection (Current)

Phase 4: C/Rust Optimization for enterprise-level processing speeds

Phase 5: Cloud Threat Intelligence Sync (e.g., AlienVault OTX integration)

👨‍💻 Project Team (Group 140)

This project was developed collaboratively by students of IIT Patna.

Sushil Singh (Roll No: 2312RES688) - GitHub Profile

Sitanshu Singh

Tanya Singh

Shubham Singh

Sourav Singh

⚠️ Disclaimer: This project is developed strictly for educational purposes and academic evaluation at IIT Patna. It should not be used as a primary substitute for commercial enterprise firewalls in production environments.

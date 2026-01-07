# Android Hardware Bridge: Remote USB-over-IP Automation

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.8%2B-yellow.svg)
![Platform](https://img.shields.io/badge/platform-Android%20ARM-green.svg)

## 📌 Project Overview
This project repurposes legacy Android hardware (ARM architecture) into a dedicated **Headless USB Server**. By utilizing low-level ADB bridging and root-privileged binary execution, it allows physical USB peripherals (sensors, printers, dongles) to be accessed remotely over a TCP/IP network as if they were locally connected.

This framework was developed to overcome hardware interfacing limitations in distributed computational environments.

## 🛠 Key Technical Achievements
*   **Root-Level System Integration:** Bypassed Android framework restrictions by executing native Linux binaries directly via `su` shell injection.
*   **Network Persistence:** Solved IP volatility issues in hybrid 2.4/5GHz environments using **MAC-based DHCP Reservation**.
*   **Headless Architecture:** Eliminated the need for physical displays (bypassing HDCP/HDMI handshake failures) by managing the node entirely via remote automation.

## 🔬 Scientific Relevance
In the context of **Computational Mathematics and Distributed Systems**, this project demonstrates a cost-effective method for **Edge Node Instrumentation**. It allows high-performance compute clusters to offload hardware polling and I/O tasks to lightweight, repurposed ARM nodes, reducing interrupt latency on the main processing units.

## 🚀 Quick Start

### Prerequisites
1.  **Hardware:** Android Device (Rooted), USB Peripheral.
2.  **Software:** Python 3.x, ADB (Android Debug Bridge) installed on the host.

### Installation

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/YourUsername/android-hardware-bridge.git
    cd android-hardware-bridge
    ```

2.  **Place the Binary:**
    Download your specific ARM binary (e.g., VirtualHere server) and place it in the `bin/` directory.

3.  **Deploy to Device (One-time Setup):**
    ```bash
    chmod +x scripts/deploy.sh
    ./scripts/deploy.sh
    ```

### Usage

Run the main automation controller to establish the link:

```bash
python src/bridge_controller.py
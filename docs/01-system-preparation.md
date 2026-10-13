# 01 - System Preparation

## 1. Objective

The objective of this project is to configure an existing
Ubuntu Linux computer as a Network Attached Storage (NAS)
server.

The server will provide centralised file storage accessible
to multiple devices on the local network, including macOS,
iOS, and other Linux computers.

The project will use Samba to implement the SMB protocol
for cross-platform file sharing.

## 2. Hardware and Software

| Component | Specification |
|-----------|---------------|
| Computer | Dell Inspiron 3583 |
| Operating System | Ubuntu 24.04.5 LTS |
| Storage | 256 GB Toshiba NVMe SSD |
| Filesystem | ext4 |
| Network Interface | Wi-Fi (wlp2s0) |
| Local IP Address | 192.168.1.50 |

## 3. Initial System Inspection

Before configuring the NAS, I inspected the existing
hardware, operating system, storage devices, and network
configuration.

### 3.1 Operating System

Command:

```bash
lsb_release -a
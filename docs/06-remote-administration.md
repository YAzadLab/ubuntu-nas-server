# 06 - Remote Administration Using SSH

## 1. Objective

Configure secure remote administration of the Ubuntu NAS
server using the Secure Shell (SSH) protocol.

This allows the server to be managed remotely from a
MacBook without requiring direct physical access.

## 2. Installing OpenSSH Server

The package lists were updated using:

```bash
sudo apt update
```

OpenSSH Server was installed using:

```bash
sudo apt install openssh-server
```

OpenSSH Server allows remote clients to establish
encrypted connections to the Ubuntu machine.

## 3. Enabling SSH

The SSH service was enabled and started using:

```bash
sudo systemctl enable --now ssh
```

The service status was verified using:

```bash
sudo systemctl status ssh
```

The expected result was:

`Active: active (running)`

## 4. Network Configuration

The Ubuntu server uses the following network configuration:

| Property | Value |
|----------|-------|
| Network Interface | wlp2s0 |
| Local IP Address | 192.168.1.50 |
| Protocol | SSH |
| Default Port | TCP 22 |

The IP address is currently assigned through the
local network and may change.

A DHCP reservation may be configured later.

## 5. Remote Connection

The following command was executed on macOS:

```bash
ssh yusuf@192.168.1.50
```

SSH authenticates the user and establishes an
encrypted connection between the MacBook and Ubuntu.

## 6. Connection Verification

The following commands were used to verify the connection:

```bash
hostname
whoami
pwd
```

These commands confirmed that the terminal session
was executing on the Ubuntu server.

## 7. Security Considerations

- SSH encrypts communication between devices.
- User authentication is required.
- SSH access is intended for the local network.
- Router port forwarding is not enabled.
- SSH keys may be configured later for stronger authentication.

## 8. Outcome

Remote administration was successfully configured,
allowing the Ubuntu server to be managed from macOS.
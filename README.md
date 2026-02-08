# secure-socks5-proxy
A secure SOCKS5 proxy built using SSH tunneling on an Ubuntu VPS hosted on DigitalOcean.

## Overview

This project demonstrates how to create a secure SOCKS5 proxy using SSH port forwarding.
The proxy routes traffic from a local machine through a remote VPS, masking the local IP
address while maintaining encrypted communication.

The goal of this project is to understand networking fundamentals, secure server access,
and practical Linux-based infrastructure used in real-world development environments.

## Architecture

Local Machine (Windows + WSL)
        |
        |  Encrypted SSH Tunnel (SOCKS5)
        |
Ubuntu VPS (DigitalOcean)
        |
        |
     Internet

## Technologies Used

- Ubuntu 22.04 (VPS)
- DigitalOcean Droplet
- OpenSSH
- SOCKS5 Proxy (SSH Dynamic Port Forwarding)
- UFW Firewall
- Windows Subsystem for Linux (WSL)
- Git & GitHub

## Setup Instructions

1. Provision an Ubuntu 22.04 VPS on DigitalOcean.
2. Create a non-root user and configure SSH key-based authentication.
3. Disable password-based SSH login and root access.
4. Enable firewall rules allowing only SSH traffic.
5. Establish a SOCKS5 proxy using SSH dynamic port forwarding.
6. Configure the local browser to route traffic through the SOCKS5 proxy.

## Security Considerations

- SSH key-based authentication is used instead of passwords.
- Root login is disabled to reduce attack surface.
- UFW firewall restricts inbound traffic to SSH only.
- All proxy traffic is encrypted via SSH tunneling.
- No logs or traffic inspection are performed on the server.

## Limitations

- The proxy is only active while the SSH tunnel is running.
- Traffic routing is browser-based unless configured system-wide.
- This setup is intended for learning, development, and secure access purposes.

## Use Cases

- Secure browsing on public or untrusted networks
- Protecting a local machine's IP address
- Learning Linux server administration and networking
- Development and testing of network-related applications

## What I Learned

- How SOCKS5 proxies work at the network level
- Secure Linux server configuration and hardening
- SSH tunneling and port forwarding
- Basic cloud infrastructure management
- Writing clear technical documentation

## Future Improvements

- Add autossh for automatic tunnel recovery
- Implement WireGuard for full VPN comparison
- Create a systemd service for persistent connections
- Add monitoring and alerting


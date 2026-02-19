# 🏠 Private Cloud Infrastructure & Home Lab

A robust, self-hosted server environment focusing on **data sovereignty**, **automated document processing**, and **zero-trust security**.

## 🏗 Hardware & OS
* **Host:** Repurposed Laptop (Intel i5/i7, integrated UPS-effect via battery).
* **OS:** Manjaro Linux (Rolling Release for latest kernel support and AUR flexibility).
* **Management:** Headless operation via **SSH** and **Cockpit** for resource monitoring.

## 🛡 Security Concept (Zero Trust)
Instead of traditional port forwarding, this setup utilizes a **Cloudflare Tunnel (Argo Tunnel)** to expose services securely.

* **Identity Provider:** Access is protected by Cloudflare Zero Trust authentication layers.
* **Geo-Fencing:** WAF (Web Application Firewall) rules restricted to **Germany** and **Netherlands** to minimize the attack surface.
* **Network Isolation:** All services run in isolated Docker containers, communicating through a dedicated bridge network.

## 📦 Hosted Services
* **Paperless-ngx:** Automated OCR document management system.
* **Immich:** High-performance self-hosted photo/video backup solution.
* **Cloudflare Tunnel:** Secure ingress without open inbound ports.

## 🛠 Tech Stack
- **Engine:** Docker & Docker Compose
- **Network:** Cloudflare Tunnel, Reverse Proxy logic
- **OS-Admin:** Cockpit, Systemd, Bash

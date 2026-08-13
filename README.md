# 🖥️ Home IT Lab & Container Infrastructure

A self-hosted home lab environment built on **Ubuntu Server**, designed for testing, container orchestration, network management, and system observability.

---

## 📐 Architecture & Key Features

* **OS & System Administration:** Configured and managed **Ubuntu Server (CLI)**, including physical drive mounting and file system management.
* **Container Orchestration:** Deployed and managed a multi-service stack using **Docker** and **Docker Compose**.
* **Secure Remote Access:** Configured **Tailscale (Mesh Overlay VPN)** to securely connect to the internal network from external devices without opening public ports.
* **Network & DNS Optimization:** Identified and resolved internal DNS query rate limits and network latency by configuring custom subnets (`/24`) and migrating container resolvers to **Cloudflare (1.1.1.1)**.
* **Monitoring & Observability:** 
  * **Uptime Kuma:** Automated uptime and status monitoring for hosted services.
  * **Scrutiny:** Hardware disk health tracking via **S.M.A.R.T.** data.
  * **Glances / System Tools:** Real-time CPU, RAM, and system resource monitoring.
* **Lifecycle & Maintenance:** Automated image updates using **Watchtower**, managed containers/volumes via **Portainer**, and performed system hygiene (`docker system prune`).

---

## 🛠️ Tech Stack & Tools

* **OS:** Linux Ubuntu Server (CLI)
* **Containers:** Docker, Docker Compose, Portainer, Watchtower
* **Networking & Security:** TCP/IP, DNS, Tailscale VPN
* **Monitoring:** Uptime Kuma, Scrutiny (S.M.A.R.T.), Glances
* **CLI Tools:** Bash, `top`, `docker inspect`, `ipconfig/ifconfig`

---

## 🔍 Key Troubleshooting Scenarios Solved

1. **DNS Resolution Latency:** Resolved container-level DNS timeouts by updating docker network configurations and assigning Cloudflare public resolvers.
2. **Drive Mounting & Health:** Successfully mounted secondary storage drives in Linux and integrated automated S.M.A.R.T. monitoring to detect disk degradation early.
3. **Resource Management:** Monitored CPU/RAM usage spikes and optimized container resources using Linux CLI diagnostic utilities (`top`, `Glances`).

---

## 📝 Disclaimer
*This lab is strictly used for educational, testing, and skill-building purposes in a controlled environment.*

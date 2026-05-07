# My Homelab

## About

**Welcome to my homelab!** This is what I enjoy doing on my free time for learning and for fun. This includes services I use day to day for convenience, privacy and overall just out of curiousity for how systems and protocols behave to further my understanding.

## Infrastructure

- **Protectli (OPNsense Firewall)** - Centralized location to manage DHCP Pools, Reservations, Subnetting for security and Firewall rules
- **Proxmox Cluster (3-Nodes)** - Compute lives here for services such as DNS, Proxies, Game Servers, Docker, Password Manager plus more. All providing high availability and management through one plane of glass.
- **UGREEN DXP6800 NAS** - Storage solution for holding backup snapshots of VMs, Media Server, Family Photos, etc
- **10-Port Cisco Managed Switch W/ PoE+**  Upstream Managed switch that powers my downstream 8-Port Cisco switch using PoE as well as connects and powers the TP-Link AP. Additionally used to Segment VLANs for added security and providing client connectivity. 
- **8-Port Cisco Managed Switch** Downstream managed switch providing connectivty to my 3-Node Proxmox cluster server and main workstation
- **TP-Link EAP Access Point for Wi-Fi** Provides Wi-Fi connectivity to client devices and is VLAN aware for IoT devices for included security
- **Cyberpower UPS** - Backup power supply for my network equipment in case of brownouts or blackouts, additionally a second UPS for my server gear

## Services 

- **Proxmox VE** — Bare metal hypervisor providing my services with compute in the form of LXCs, VMs and Docker containers
- **Pi-hole** — Primary DNS solution to filter ADs and block unnecessary telemetry for all clients on the network
- **Unbound** — Recursive upstream DNS resolver for privacy, security and performance without relying on a 3rd party solution
- **NGINX (reverse proxy)** - Used along Pi-Hole for HTTP(s) routing for local IPs to resolve to friendly URLs for easier management instead of IP:Port
- **Wazuh** *(currently configuring)* - SIEM for ingesting logs from my Linux workstation, Windows workstation and Firewall. Provides visibility into network activity for the purposes of identifying security threats and vulnerabilities that may be present
- **OPNsense** — Main center of control for networking providing DHCP, reservations, network segmentation and configured with directing DNS to Pi-hole
- **Docker** — Container runtime for Vaultwarden, Nginx, Zabbix and Valheim
- **Kali-Linux + Metasploit** *(currently configuring)* - VM to self teach red team and blue team activities and to understand better how to secure infrastructure

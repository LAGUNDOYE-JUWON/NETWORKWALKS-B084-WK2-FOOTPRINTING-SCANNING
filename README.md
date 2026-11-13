# NETWORKWALKS-B084-WK2-FOOTPRINTING-SCANNING
practical  experience on active and passive web footprinting, DNS enumeration, subnet scanning ARP interrogation, and topology mapping  networkwalks Week2  
## Footprinting & Network Scanning Report

## Description & Overview
This report documents the practical security analysis executed during Week 2 (W2-PM1 and W2-PM5) under the Networkwalks Cybersecurity Internship Program. All testing was executed in full compliance with explicit authorization within scoped target environments (networkwalks.com and isolated virtual lab subnets). The primary objective was to perform passive and active domain reconnaissance, gather target infrastructure metadata, discover active hosts on local subnets, analyze host routing, map network topology, and extract physical MAC identifiers via ARP table interrogation. Unapproved distribution or misuse of this technical data is strictly prohibited.
#  Reconnaissance & Network Scanning Report

![Category](https://img.shields.io/badge/Category-Cybersecurity-blue)
![Program](https://img.shields.io/badge/Program-Networkwalks--B084-green)
![Phases](https://img.shields.io/badge/Phases-Recon%20%26%20Scanning-orange)
![Purpose](https://img.shields.io/badge/Purpose-Educational-lightgrey)

Final Week 2 project report for the **Networkwalks** cybersecurity program, documenting Phase 1 (Reconnaissance & Footprinting) and Phase 2 (Scanning & Network Discovery) using Kali Linux tools and Zenmap.

---

## 🚧 Project Overview

| Field | Detail |
|---|---|
| **offensive security analyst** | Lagundoye Juwon Akeem |
| **Program / Batch** | Networkwalks-B084 |
| **Date** | 9th November, 2026 |
| **Modules Completed** | W2-PM1 (Multiple Kali Tools), W2-PM5 (Zenmap Scanning) |
| **Client / Target** | 1. Networkwalks (written permission secured)<br>2. Personal local LAN network |
| **Permission Secured from Client?** | Yes |
| **Phases Covered** | Phase 1: Reconnaissance & Footprinting<br>Phase 2: Scanning & Network Discovery |

---

## 🎯 1. Liability Disclaimer

The activities documented in this report were conducted strictly on systems and devices for which prior written authorization was obtained, or on personally owned hardware. The contents of this document are intended strictly for educational and research purposes. The instructor, author, and Networkwalks assume no liability for the misuse or misapplication of this knowledge; all subsequent actions taken by the reader are their sole responsibility.

Unauthorized system access constitutes a criminal offense in most jurisdictions, regardless of whether data or systems are damaged, and can result in severe legal penalties, significant fines, career impact (employment termination), and a permanent criminal record.

> ⚠️ **Note:** Authorization must be secured from Networkwalks before performing reconnaissance and footprinting.



## ☄️ 2. Introduction 

As part of my Networkwalks internship program (week 2), this report provides a comprehensive analysis of the Footprinting/Reconnaissance phases targeting the networkwalks.com domain and subsequent scanning of the local network utilizing Zenmap. By leveraging a combination of Kali Linux tools and Zenmap, this assessment simulates how a malicious actor actively maps live network hosts. The methodology mirrors an attacker's lifecycle, transitioning from passive data gathering (W2-PM1) to active host discovery (W2-PM5).

## 💡 Footprinting

All footprinting commands were executed within a Kali Linux environment.

## 🔎 Scanning activities

Were performed via Zenmap on a windows host (pc).

## 📝 Methodology, analysis framework, and documentation

To ensure reproducibility and rigorous documentation, every technical step outlines the exact commands utilized, corresponding system output, verification screenshots, and a brief analytical note from the attackers point of view regarding the security implications of the exposed data.

## ⚒️ 3. Tools Used
Each tool used and its purpose can be found in the table below.
---
|Tool/commands |	Purpose|
|---|---|
|**Kali Linux**|Operating system deployed to conduct initial reconnaissance and information gathering.|
|**Windows OS**|	Host Operating systems utilized for networking activities including network mapping via Zenmap.|
|**WHOIS**|	Queries or Finds domain registration details such as registration ownership, critical dates, and authoritative name servers.|
|**whatweb**|	Identifies and fingerprints web technologies, including servers, CMS - content management system, plugins, and IP.|
|**nslookup**|	Performs DNS lookup to resolve target domain names to their respective IP address|
|**curl -I**|	Fetches, analyses, and reads the HTTP response headers of the website.|
|**wafw00f**|	Probes the web application to detect the presence and type of Web Application Firewall (WAF) present.|
|**dnsrecon**|	Enumerate or discovers all DNS records (NS, MX, SPF, TXT, SRV).|
|**Zenmap (Nmap GUI)**|	Scan the local subnet to find live hosts, active IP addresses, and MAC addresses.|
|**Windows CMD**|	Local IP and MAC address identification via a command line interface.|

---

## 🛡️Activities Performed

## 4. Footprinting & Reconnaissance Attacks With Multiple Kali Tools
## 4.1. Background
Reconnaissance (also called as footprinting) is the first step in any real attack or security test. Before touching a target, an attacker quietly collects as much public information about it as possible. This includes who owns the domain, its real IP address, the hosting provider, the web technologies it runs, its DNS and mail records, and whether a firewall is protecting it. All of this comes from information the target has already made public, so the target never even knows it is being studied. This is why recon is powerful and very hard to detect.

> **⚠️** In this lab, the live website networkwalks.com was footprinted.

## 💡4.2. Footprinting & Reconnaissance
I performed reconnaissance against the networkwalks.com domain using six Kali Linux commands:

`dnsrecon`
`nslookup`
`whatweb`
`curl -I`
`whois`
`Nmap/Zenmap`


> **⚠️** Note: Each tool was used to collect a different type of information about the target as seen in table 3 above.

## 4.2.1. WHOIS
WHOIS was used to obtain publicly available domain registration information and identify the domain’s name servers. The results provided information about the domain registration and hosting infrastructure.
>  Command used: `whois networkwalks.com`




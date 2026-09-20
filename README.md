# NETWORKWALKS-B083D-WK2-PM1-5-FOOTPRINTING-AND-NETWORK-SCANNING
# Week 2 Cybersecurity Footprinting and Network Scanning Projects

## Overview

This repository contains my Week 2 cybersecurity practical work completed during the Networkwalks cybersecurity training program.

The projects focus on **footprinting, reconnaissance, information gathering, and network scanning** using different cybersecurity tools and techniques.

Five practical modules were completed:

1.Footprinting and reconnaissance with WHOIS, WhatWeb, nslookup, cURL, DNSRecon and WAFW00F
2.Footprinting and reconnaissance with the Google Hacking Database (GHDB)
3.Footprinting with Maltego
4.Footprinting and reconnaissance with theHarvester
5.Network scanning with Zenmap/Nmap

The completed work in this repository covers:

* **Project 1 — Footprinting & Reconnaissance**
* **Project 4 — Footprinting & Reconnaissance with theHarvester**
* **Project 5 — Network Scanning with Zenmap/Nmap**

Projects related to GHDB and Maltego are included only as reference topics and were not completed as part of my submitted Week 2 work.

All activities were performed in a controlled lab environment for educational and authorized cybersecurity practice.

---

## Learning Objectives

Through these practical exercises, I learned how to:

* Understand the concept of footprinting and reconnaissance.
* Collect publicly available information about a target.
* Perform passive and active reconnaissance.
* Gather DNS and domain-related information.
* Identify web technologies and server information.
* Inspect HTTP headers and web-server responses.
* Identify possible Web Application Firewall (WAF) protection.
* Use theHarvester for information gathering from multiple sources.
* Perform network discovery using Zenmap/Nmap.
* Identify live hosts on a network.
* Identify IP addresses and MAC addresses where available.
* Understand basic network topology and discovered devices.
* Document reconnaissance and scanning results.
* Understand how information gathered during reconnaissance can help both attackers and defenders.

---

# Project 1 --- Footprinting & Reconnaissance

## Tools

The following tools were used during the footprinting and reconnaissance activities:

* WHOIS
* WhatWeb
* nslookup
* cURL
* DNSRecon
* WAFW00F

## Activities

The objective of this project was to understand how information about a domain or web application can be collected during the reconnaissance phase.

### WHOIS

WHOIS was used to gather domain registration and ownership-related information available through public records.

The information collected can help identify details such as:

* Domain information
* Registrar information
* Registration details
* Name servers
* Domain status

  <img width="1919" height="1024" alt="Screenshot 2026-09-18 192848" src="https://github.com/user-attachments/assets/0f10416c-6f3f-4943-8b45-a053c703a65a" />


### WhatWeb

WhatWeb was used to identify technologies associated with a target website.

It can help identify information such as:

* Web server technologies
* Frameworks
* Content management systems
* JavaScript libraries
* Other technologies detected from the website
* 
<img width="1912" height="230" alt="Screenshot 2026-09-19 115412" src="https://github.com/user-attachments/assets/c010f322-c752-4ef4-a4db-6b5fca44aec6" />


### nslookup

The `nslookup` command was used to perform DNS queries.

Example:

```bash
nslookup <target>
```
<img width="565" height="145" alt="Screenshot 2026-09-19 110446" src="https://github.com/user-attachments/assets/10924eb9-c179-4d29-bf4e-9889f48d61e3" />

This helped understand how domain names are resolved to IP addresses and provided basic DNS information.

### cURL

`cURL` was used to interact with the target web server and inspect HTTP responses.

Example:

```bash
curl -I <target>
```
<img width="1919" height="275" alt="Screenshot 2026-09-19 115520" src="https://github.com/user-attachments/assets/68d9c5dd-a090-4c3d-92e8-4cbd02ec8e09" />


This helped examine HTTP response headers and understand information returned by the web server.

### DNSRecon

DNSRecon was used to perform DNS reconnaissance and gather DNS-related information.

Example:

```bash
dnsrecon -d <target>
```
<img width="1915" height="452" alt="Screenshot 2026-09-19 115832" src="https://github.com/user-attachments/assets/c823ba76-8d35-4b53-85c5-a138478fcc2f" />


The activity helped demonstrate how DNS information can reveal useful details about a domain and its infrastructure.

### WAFW00F

WAFW00F was used to check whether a Web Application Firewall could be detected protecting the target.

Example:

```bash
wafw00f <target>
```
<img width="1252" height="352" alt="Screenshot 2026-09-19 115625" src="https://github.com/user-attachments/assets/aebfbde9-6ffe-4d2d-9fbb-7cf563013919" />


This demonstrated how security technologies protecting web applications can sometimes be identified through reconnaissance.

## Key Observations

During this project, I observed that different reconnaissance tools provide different types of information.

Some tools focused on:

* Domain information
* DNS records
* Web technologies
* HTTP headers
* Server information
* WAF detection

Using multiple tools together provides a broader understanding of the target environment than relying on a single tool.

## Security Relevance

Footprinting is an important phase of cybersecurity assessment because publicly available information can help identify an organization's attack surface.

From a defensive perspective, organizations should understand what information about their infrastructure is publicly exposed and minimize unnecessary information disclosure.

---

# Project 2 --- Footprinting with GHDB

Google Hacking Database (GHDB) can be used to understand how specially crafted search queries can locate publicly indexed information.

The activity demonstrates how search engines may expose information that organizations unintentionally make publicly accessible.

**Status:** Not completed as part of my submitted Week 2 practical work.

---

# Project 3 --- Footprinting with Maltego

Maltego is a reconnaissance and information-gathering tool that can be used to visualize relationships between domains, people, infrastructure, and other publicly available information.

It can help security professionals understand connections between different entities during reconnaissance.

**Status:** Not completed as part of my submitted Week 2 practical work.

---

# Project 4 --- Footprinting & Reconnaissance with theHarvester

## Tool

* theHarvester

TheHarvester is a reconnaissance tool used to gather publicly available information about a target from different sources.

It can be useful for collecting information such as:

* Email addresses
* Hostnames
* Subdomains
* IP addresses
* URLs
* Other publicly available information
<img width="1919" height="956" alt="Screenshot 2026-09-19 232007" src="https://github.com/user-attachments/assets/a1bb5595-5ca6-41e8-a634-80f33ff7e4dc" />

---

## Task 1 --- Baidu

The first activity involved using **Baidu** as a search source with theHarvester.

Example command:

```bash
theHarvester -d microsoft.com -l 1000 -b baidu
```
<img width="1919" height="1019" alt="Screenshot 2026-09-20 125247" src="https://github.com/user-attachments/assets/dc1fa27a-8f4e-430f-9704-de26440ca6a2" />

The command was used to search for publicly available information associated with the target.

### Result

The output generated by theHarvester was examined to identify information discovered from the selected source.

**Evidence:**
The actual command output and screenshots are included in the repository.

---

## Task 2 --- Multiple Sources

TheHarvester can also perform reconnaissance using multiple available data sources.

Example:

```bash
theHarvester -d microsoft.com -b all
```
<img width="1919" height="1028" alt="Screenshot 2026-09-20 125900" src="https://github.com/user-attachments/assets/db90a8e3-106b-48a3-9d3f-d6a55669ff6a" />


The purpose of this activity was to understand how using different sources can provide additional information about a target.

The results were reviewed for publicly available:

* Email addresses
* Hosts
* IP addresses
* URLs
* Other domain-related information

### Result

The information returned by theHarvester was documented using screenshots and command outputs from the practical exercise.

## Security Relevance

TheHarvester demonstrates how much information can potentially be collected from publicly available sources without directly interacting with internal systems.

For defenders, this highlights the importance of:

* Limiting unnecessary public information.
* Reviewing publicly exposed email addresses and infrastructure details.
* Monitoring exposed subdomains and hosts.
* Understanding the organization's external attack surface.
* Performing regular reconnaissance from an external perspective.

---

# Project 5 --- Network Scanning with Zenmap/Nmap

## Tools

* Zenmap
* Nmap

## Activities

This project focused on network discovery and scanning using **Zenmap**, the graphical interface for Nmap.

The objective was to identify devices available within the authorized lab network and understand basic network topology.

The scanning activity helped identify information such as:

* Live hosts
* IP addresses
* MAC addresses where available
* Host information
* Open ports where detected
* Network structure and relationships

Nmap was also used through Zenmap to perform network discovery.

The scan was performed against the authorized lab network/environment.

## Scan Result

The completed scan produced information about the hosts discovered within the lab network.

The actual scan results, including the discovered hosts and network details, are documented through the screenshots and Zenmap output included in this repository.
<img width="1109" height="1024" alt="Screenshot 2026-09-20 134922" src="https://github.com/user-attachments/assets/df95961f-5469-40c1-ba4f-b1d79d9accf3" />
<img width="808" height="735" alt="Screenshot 2026-09-20 135010" src="https://github.com/user-attachments/assets/f280f5d3-4730-4254-8287-46daaa84f0b7" />
<img width="1099" height="1022" alt="Screenshot 2026-09-20 135118" src="https://github.com/user-attachments/assets/70a2735b-29f7-4dcd-84cb-e81b2059ff2f" />
<img width="1627" height="969" alt="Screenshot 2026-09-20 135458" src="https://github.com/user-attachments/assets/3955c6b6-d7ac-4fd1-be56-f0edd038a020" />
<img width="1919" height="1020" alt="Screenshot 2026-09-20 135629" src="https://github.com/user-attachments/assets/7f0eee23-a535-4ae3-b0aa-d565b9702e0e" />





The results were used to understand:

* Which hosts were active.
* The IP addresses associated with discovered devices.
* MAC addresses where they were available.
* Basic information about the network.
* How devices can be visualized as part of a network topology.

### Network Topology

The Zenmap scan was also used to understand the relationship between discovered hosts and the network.

The topology generated from the scan is included as evidence in the repository.

> **Note:** The number of hosts and specific IP/MAC addresses shown in the screenshots represent my actual lab environment and may differ from other reference repositories.

## Security Relevance

Network scanning is an important part of security assessment because it helps identify systems that are reachable within a network.

From a defensive perspective, network discovery can help organizations:

* Identify unauthorized devices.
* Maintain an updated asset inventory.
* Detect unexpected hosts.
* Identify unnecessary exposed services.
* Understand network segmentation.
* Investigate potentially vulnerable systems.

---

# Evidence

The repository contains evidence of the completed practical activities, including screenshots and scan results.

The evidence corresponds to the three completed projects:

* **Project 1 — Footprinting & Reconnaissance**
* **Project 4 — theHarvester**
* **Project 5 — Zenmap/Nmap**
~~(all evidences are link according to their respective project description)

Typical evidence includes:

* Command outputs
* Reconnaissance results
* theHarvester results
* Zenmap scan results
* Network topology
* Screenshots from the practical exercises

The screenshots and results in this repository represent my own lab environment and practical work.

---

# Tools & Technologies

## Footprinting & Reconnaissance

* WHOIS
* WhatWeb
* nslookup
* cURL
* DNSRecon
* WAFW00F

## Information Gathering

* theHarvester
* Search-engine based reconnaissance

## Network Scanning

* Zenmap
* Nmap

## Environment

* Kali Linux
* VirtualBox
* Lab Network Environment

---

# Key Takeaways

1. Footprinting helps security professionals understand the publicly visible attack surface of a target.

2. Different reconnaissance tools provide different types of information, so multiple tools can be useful during an assessment.

3. DNS information can reveal useful details about an organization's infrastructure.

4. Web technologies and HTTP headers can provide information about the technologies used by a web application.

5. theHarvester demonstrates how publicly available information can be collected from multiple sources.

6. Network scanning helps identify active hosts and understand the structure of an authorized network.

7. Zenmap provides a graphical way to perform Nmap-based scanning and visualize network information.

8. Reconnaissance and network scanning should always be performed only against systems and networks where authorization has been provided.

---

# Defensive Recommendations

Organizations can reduce reconnaissance-related exposure by:

* Regularly reviewing publicly available domain and DNS information.
* Removing unnecessary publicly exposed information.
* Monitoring subdomains and externally accessible hosts.
* Avoiding unnecessary disclosure of server and technology information.
* Reviewing HTTP response headers for excessive information disclosure.
* Maintaining an accurate inventory of authorized network devices.
* Monitoring for unknown or unauthorized hosts.
* Restricting unnecessary open ports and services.
* Performing regular security assessments of the external attack surface.

---

# Conclusion

Week 2 provided practical exposure to the reconnaissance and network discovery stages of cybersecurity.

Through the completed footprinting, theHarvester, and Zenmap/Nmap activities, I learned how publicly available information and network-level information can be collected and analyzed during a security assessment.

These exercises also helped me understand the importance of reconnaissance from a defensive perspective, especially for identifying exposed information, systems, and services that could increase an organization's attack surface.

---

# Disclaimer

All activities documented in this repository were performed for **educational and authorized cybersecurity training purposes only**.

The techniques demonstrated should only be used against systems, applications, domains, and networks where explicit permission has been provided.

The author is not responsible for any misuse of the techniques or tools presented in this repository.

---

# Author

**Javeriya Tahreem**

Cybersecurity Student | Networkwalks Trainee (B083D)

Week 2 Cybersecurity & Ethical Hacking Practical Projects

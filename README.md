# Kali Metasploit Lab – Vulnerability Assessment and Penetration Testing

## Project Overview

This project demonstrates a practical vulnerability assessment and penetration testing workflow using Kali Linux and Metasploitable 2 in an isolated virtual lab environment.

The project explores network reconnaissance, vulnerability identification, controlled exploitation, post-exploitation enumeration, and network traffic analysis.

It aims to understand common security weaknesses, demonstrate their potential impact, and identify appropriate security recommendations.

## Objectives

- Perform network reconnaissance and identify open ports and services.
- Identify potential vulnerabilities in exposed services.
- Use the Metasploit Framework to perform controlled exploitation.
- Verify access and examine target system information.
- Capture and analyze network traffic.
- Document security findings and possible remediation measures.

## Lab Environment

| Component | Details |
|---|---|
| Attacker Machine | Kali Linux |
| Target Machine | Metasploitable 2 |
| Virtualization | Oracle VirtualBox |
| Network Type | Host-Only Network |
| Attacker IP | 192.168.56.102 |
| Target IP | 192.168.56.101 |

## Tools and Technologies

- **Nmap:** Network scanning and service detection.
- **SearchSploit:** Searching publicly documented exploit references.
- **Metasploit Framework:** Controlled vulnerability exploitation.
- **tcpdump:** Network packet capture.
- **Wireshark:** Network traffic analysis.
- **Linux Commands:** System and network enumeration.

## Project Experiments

### Experiment 01 – Network Reconnaissance

Performed network discovery and port scanning using Nmap to identify active services and their versions on the target machine.

**Key activities:**
- Host discovery and connectivity testing.
- Open port identification.
- Service and version detection.
- Default Nmap scripting engine scans.

### Experiment 02 – Vulnerability Assessment

Investigated exposed services and potential security weaknesses using SearchSploit and Nmap vulnerability detection scripts.

**Key activities:**
- FTP anonymous login assessment.
- vsftpd 2.3.4 vulnerability research.
- Samba security assessment.
- UnrealIRCd vulnerability research.
- Bind-shell service examination.
- Targeted vulnerability scanning.

### Experiment 03 – Controlled Exploitation

Used the Metasploit Framework to test the vsftpd 2.3.4 backdoor vulnerability against the isolated target.

**Key findings:**
- Successfully established a command shell session.
- Obtained root-level access.
- Verified privileges using system identification commands.

### Experiment 04 – Post-Exploitation and Traffic Analysis

Performed basic system enumeration and examined network communication between the attacker and target machines.

**Key activities:**
- User and privilege identification.
- Operating system and hostname identification.
- Network configuration examination.
- Running process and listening port inspection.
- Packet capture using tcpdump.
- Traffic inspection using Wireshark.

## Key Findings

- Multiple network services were exposed on the target machine.
- Anonymous FTP access was permitted.
- FTP communication used unencrypted connections.
- Potential weaknesses were investigated using vulnerability assessment tools.
- The vsftpd 2.3.4 backdoor was successfully exploited in the isolated lab.
- Root-level access was verified.
- Network traffic was captured for further analysis.

## Project Structure

```text
Kali-Metasploit-Lab/
│
├── Experiments/
│   ├── 1-Reconnaissance.md
│   ├── 2-Vulnerability Assessment.md
│   ├── 3-Controlled Exploitation.md
│   └── 4-Post-Exploitation and Traffic-Analysis.md
│
├── Screenshots/
│   ├── reconnaissance/
│   ├── vulnerability assessment/
│   ├── controlled exploitation/
│   └── post-exploitation and traffic analysis/
│
├── Results/
│   ├── reconnaissance/
│   ├── vulnerability assessment/
│   ├── controlled exploitation/
│   └── post-exploitation and traffic analysis/
│
└── README.md
```

## Security Recommendations

- Disable anonymous FTP access unless explicitly required.
- Replace outdated and vulnerable services with supported versions.
- Use encrypted communication protocols such as SFTP and SSH.
- Restrict unnecessary open ports and services.
- Apply regular security updates and patches.
- Monitor network activity and investigate suspicious connections.
- Follow the principle of least privilege.

## Learning Outcomes

Through this project, practical experience was gained in:

- Network reconnaissance and port scanning.
- Vulnerability assessment and exploit research.
- Metasploit module configuration and controlled exploitation.
- Linux command-line enumeration.
- Network packet capture and analysis.
- Technical documentation and security reporting.

## Disclaimer

This project was conducted strictly for educational purposes in an isolated virtual lab environment using intentionally vulnerable systems.

All testing was performed on the authorized Metasploitable 2 virtual machine. These techniques must only be used on systems for which explicit authorization has been obtained.
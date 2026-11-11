# Experiment 01: Network Reconnaissance Using Nmap

## 1. Objective
To perform network reconnaissance on an intentionally vulnerable target machine using Nmap and identify its open ports, running services and versions.

## 2. Lab Environment
- Attacker Machine: Kali Linux
- Target Machine: Metasploitable 2
- Virtualization: Oracle VirtualBox
- Network Configuration: Host-Only Adapter
- Target IP: 192.168.56.101
- Tool Used: Nmap 7.95

## 3. Methodology
1. Identified the IP addresses of both virtual machines.
2. Checked connectivity between Kali Linux and Metasploitable 2.
3. Performed a basic port scan using Nmap.
4. Identified running services and their versions.
5. Used default Nmap scripts to collect additional information.
6. Saved the scan output for documentation and analysis.

## 4. Commands Used

```bash
ip -br addr
ifconfig
ping -c 4 192.168.56.101
nmap 192.168.56.101
nmap -sV 192.168.56.101
nmap -sC -sV 192.168.56.101 -oN nmap-scan.txt
```

## 5. Observations

1. The target machine was reachable at 192.168.56.101.
2. Nmap identified 23 open TCP ports among the default 1,000 scanned ports.
3. Multiple services were detected, including FTP, SSH, Telnet, HTTP, SMB, MySQL and PostgreSQL.
4. Anonymous FTP login was permitted on port 21.
5. Several outdated services and protocols were identified.
6. Port 1524 was identified as a Metasploitable root shell.
7. The SMTP service supported the deprecated SSLv2 protocol.
8. Nmap collected information about the target system and its network services.

## 6. Results

The reconnaissance scan successfully identified the target machine and detected 23 open TCP ports. Service and version detection provided information about the applications running on these ports.

The results revealed several potential security weaknesses, including anonymous FTP access, outdated services, legacy protocols and an exposed bind shell.

These findings will be investigated further during the vulnerability assessment phase.

## 7. Conclusion

The network reconnaissance experiment was successfully completed using Nmap. The scan provided an overview of the target machine's exposed network services and potential security weaknesses. The collected information will be used in the next phase of vulnerability assessment.

## 8. Evidence

Evidence screenshots and the original Nmap scan output are stored in the project folders.
# Experiment 04: Post-Exploitation and Traffic Analysis

## 1. Objective

To perform basic post-exploitation analysis on the Metasploitable 2 virtual machine and examine network traffic generated during communication between Kali Linux and the target system.

## 2. Lab Environment

- **Attacker Machine:** Kali Linux
- **Target Machine:** Metasploitable 2
- **Virtualization:** Oracle VirtualBox
- **Network Configuration:** Host-Only Network
- **Attacker IP:** 192.168.56.102
- **Target IP:** 192.168.56.101
- **Tools Used:** Metasploit Framework, tcpdump, Wireshark, Nmap

## 3. Methodology

The experiment was divided into two stages.

### A. Post-Exploitation Analysis

1. Checked the availability of the previously established Metasploit session.
2. Established a new command shell session when the previous session was unavailable.
3. Executed system identification commands.
4. Examined user privileges, operating system information, network configuration, running processes and listening ports.
5. Saved the command output for documentation.

### B. Network Traffic Analysis

1. Identified the active Kali network interface.
2. Started packet capture using tcpdump.
3. Generated ICMP traffic using ping.
4. Generated TCP traffic using Nmap.
5. Saved the captured packets in PCAP format.
6. Examined the captured traffic using tcpdump and Wireshark.
7. Applied display filters to inspect relevant network packets.

## 4. Commands Used

### Post-Exploitation Commands

```bash
whoami
id
hostname
uname -a
pwd
ip addr
ip route
cat /etc/issue
ps aux
netstat -tuln
```

### Network Traffic Analysis Commands

```bash
ip -br addr
```

```bash
sudo tcpdump -i any -nn host 192.168.56.101 -w /mnt/post-exploitation-traffic-analysis/lab-traffic.pcap
```

```bash
ping -c 4 192.168.56.101
```

```bash
nmap -sT -p 21,22,80,445,6667 192.168.56.101
```

```bash
sudo tcpdump -nn -r /mnt/post-exploitation-traffic-analysis/lab-traffic.pcap
```

```bash
wireshark /mnt/post-exploitation-traffic-analysis/lab-traffic.pcap
```

## 5. Observations

- The Metasploit command shell was used to inspect the target system.
- System identification commands were executed to examine the target's identity and operating system.
- Network interface and routing information were examined.
- Running processes and listening network ports were inspected.
- Network packets were captured using tcpdump.
- ICMP traffic was generated using ping.
- TCP traffic was generated using Nmap.
- The saved packet capture was examined using Wireshark and relevant display filters.

## 6. Results

Post-exploitation enumeration commands were used to gather information about the target system, including user privileges, operating system details, network configuration and running processes.

Network traffic was captured and saved in PCAP format. The captured packets were examined using tcpdump and Wireshark to study communication between the Kali Linux attacker machine and the Metasploitable 2 target.

The experiment demonstrated how system enumeration and network traffic analysis can help understand activities performed during and after a security compromise.

## 7. Conclusion

The experiment demonstrated basic post-exploitation enumeration and network traffic analysis in an isolated virtual lab environment.

System information was collected through the established command shell, while tcpdump and Wireshark were used to capture and inspect network communication.

These activities highlighted the importance of monitoring system activity, analyzing network traffic and identifying suspicious communication during security investigations.

## 8. Evidence

The following evidence is stored in the project folders:

- Post-exploitation command output.
- System and network information screenshots.
- Running process and listening port information.
- tcpdump packet capture output.
- PCAP file containing captured network traffic.
- Wireshark packet analysis screenshots.
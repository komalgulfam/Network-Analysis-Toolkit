
# Lab 02 - Advanced Port Scanning & Timing

## Objective
Learn how to scan specific port ranges, apply TCP scan flags, and tune scan speeds.

## Environment
- Operating System: Kali Linux
- Tool: Nmap
- Privileges: Root / sudo

## Tasks Performed

### 1. SYN Stealth Scan
```bash
sudo nmap -sS TARGET_IP
#result
Performed a half-open TCP scan to detect open ports quietly.
#2. Comprehensive Port Range Scan
nmap -p1-1023 TARGET_IP
nmap -p- TARGET_IP
#3. FIN and Xmas Scans
nmap -sF TARGET_IP
nmap -sX TARGET_IP
#Result
Sent manipulated packet flags to analyze firewall and port responses.
#4. Speed & Timing Control
nmap -T4 -p- TARGET_IP
#Result

Accelerated scan execution using aggressive timing templates.

#Commands Used
nmap -sS
nmap -sF
nmap -sX
nmap -p
nmap -T

#What I Learned
Difference between SYN, FIN, and Xmas scan techniques.
How to scan full port ranges efficiently.
Managing network traffic impact using timing templates.

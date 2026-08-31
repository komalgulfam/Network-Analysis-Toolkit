# Nmap Command Cheat Sheet

This file contains Nmap commands and options practiced during network scanning modules.

## Basic Scanning & Output Formats
- `ls`: List directory contents
- `/usr/share/nmap/scripts/`: Default path for Nmap scripts
- `nmap -oA FILENAME IPADDRESS`: Save output result in all 3 major formats
- `nmap -oN FILENAME IPADDRESS`: Save output result in human-readable normal format
- `nmap -oG FILENAME IPADDRESS`: Save output result in grepable format

## Command Switches & Flags
- `-vv`: See level 2 verbose details
- `-O`: Detect target operating system
- `-Pn`: Treat all hosts as online -- skip host discovery
- `-sn`: Host discovery only (no port scanning, lists online IPs)
- `-sU`: UDP port scan
- `-sS`: TCP SYN port scan (default/stealth)
- `-sF`: TCP FIN scan
- `-sX`: TCP Xmas scan
- `-Sc` / `-sC`: Run default scripts for extra details
- `-p-`: Scan all 65,535 ports
- `-F`: Scan first 100 common ports
- `-r`: Scan ports sequentially (in order)
- `-h`: Display help menu and switches
- `-f`: Send fragmented packets to evade firewalls
- `--mtu NUM`: Specify custom MTU (must be multiple of 8)
- `--scan-delay TIMEms`: Add delay between packets
- `--badsum`: Send packets with a fake/bad checksum

## Port Selection Options
| Option | Meaning |
| :--- | :--- |
| `-p22,80,443` | Specific ports |
| `-p1-1023` | Port range |
| `-p-` | All 65,535 ports |
| `-F` | Top 100 common ports |
| `--top-ports 10` | Top 10 common ports |

## Timing Templates (-T0 to -T5)
| Switch | Meaning |
| :--- | :--- |
| `-T0` | Slowest (Paranoid) |
| `-T1` | Very slow (Sneaky) |
| `-T2` | Polite |
| `-T3` | Normal / Default |
| `-T4` | Fast / Aggressive |
| `-T5` | Fastest (Insane) |

## Performance & Rate Tuning
- `--min-rate`: Minimum desired packets/sec
- `--max-rate`: Maximum packets/sec
- `--min-parallelism`: Minimum simultaneous probes
- `--max-parallelism`: Maximum simultaneous probes

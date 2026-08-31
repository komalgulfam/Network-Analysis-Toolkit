# Nmap Scanning & Output Concepts

## Output Formats
- `-oA`: Save output results in all 3 major formats simultaneously.
- `-oN`: Save output results in a human-readable normal format.
- `-oG`: Save output results in a grepable format for easy parsing.

## Basic Scanning Switches
- `-vv`: Level 2 verbose detail for in-depth output.
- `-O`: Target operating system detection.
- `-Pn`: Treat all hosts as online, skipping host discovery.
- `-sn`: Host discovery only (ping scan, lists online IPs without port scanning).
- `-sU`: UDP port scan.
- `-sS`: TCP SYN stealth port scan.
- `-sF`: TCP FIN scan.
- `-sX`: TCP Xmas scan.
- `-sC` / `-Sc`: Run default scripts for extra details.
- `-p-`: Scan all 65,535 ports.
- `-F`: Scan the first 100 common ports.
- `-r`: Scan ports sequentially in order.
- `-h`: Display help menu and command switches.

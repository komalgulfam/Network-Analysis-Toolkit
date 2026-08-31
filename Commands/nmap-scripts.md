# Nmap Scripting Engine (NSE) & Advanced Scanning

## Script Searching & Management
- `grep -l 'FIRSTWORD.*SECONDWORD' /usr/share/nmap/scripts/`: Find scripts matching patterns
- `ls /usr/share/nmap/scripts/*.nse`: Check file names of specific categories
- `nmap --script-help CATEGORYNAME`: Check category descriptions
- `nmap --script=CATEGORY TARGET_IP`: Run all scripts of a specific category
- `nmap --script SCRIPTNAME --script-args SCRIPTNAME.username=USER,SCRIPTNAME.password=PASS TARGETIP`: Run script with authentication arguments
- `grep "WORD" /usr/share/nmap/scripts/script.db`: Search script details in database
- `ls /usr/share/nmap/scripts/*WORD*`: Search scripts by keyword in filename
- `sudo wget -O /usr/share/nmap/scripts/SCRIPTNAME.nse URL`: Download custom script from URL
- `sudo nmap --script-updatedb`: Update script database after adding new scripts

## Target & IP Range Scanning
- `nmap -iL FILENAME`: Scan list of IPs from a file
- `10.11.12.15-20`: Scan specific IP range
- `nmap TARGET1 TARGET2 TARGET3`: Scan multiple targets at once
- `nmap -p from-to TARGETIP`: Scan custom port range
- `nmap -sL 10.10.10.1-5`: List targets only (no actual scanning)
- `nmap -sL -n 192.168.1.1-5`: List targets without DNS lookup

## Host Discovery (Ping Scans)
- `nmap -sn TARGETIPS`: Ping scan (no port scan)
- `nmap -PR -sn TARGETIPS`: ARP scan (local subnet only)
- `nmap -PE -sn IPRANGE`: ICMP Echo request scan
- `nmap -PP -sn IPRANGE`: ICMP Timestamp request scan
- `nmap -PM -sn IPRANGE`: ICMP Address Mask scan
- `nmap -PS -sn IPRANGE`: TCP SYN Ping scan
- `nmap -PS21 -sn TARGET`: TCP SYN ping on specific port (e.g., port 21)
- `nmap -PS21-25 -sn TARGET`: TCP SYN ping on port range
- `nmap -PA -sn IPRANGE`: TCP ACK Ping scan
- `nmap -PU -sn IPRANGE`: UDP Ping scan

## Reverse DNS & Subnet Calculation
- `nmap -R TARGETIPS`: Always do reverse DNS resolution
- `nmap --dns-servers 8.8.8.8 TARGETIPS`: Use custom DNS server
- `nmap -n TARGETIPS`: Disable reverse DNS resolution
- *Subnet Calculation Example:* For `10.10.10.13/29`, subnet mask binary ends in `11111000` ($248$), block size = $256 - 248 = 8$ (Ranges: 0-7, 8-15, etc.)

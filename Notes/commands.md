# Network Toolkit Commands - Quick Revision

## Nmap Scanning & Discovery
```bash
nmap -oA FILENAME IP
nmap -sn TARGET_IPS
nmap -PR -sn TARGET_IPS
nmap -sS TARGET_IP
nmap -sU TARGET_IP
nmap -sF TARGET_IP
nmap -sX TARGET_IP
nmap -p- TARGET_IP
nmap -F TARGET_IP
nmap -T4 TARGET_IP
Nmap Scripting Engine (NSE)
Bash
grep -l 'FIRSTWORD.*SECONDWORD' /usr/share/nmap/scripts/*.nse
nmap --script-help CATEGORYNAME
nmap --script=CATEGORY TARGET_IP
nmap --script SCRIPTNAME --script-args SCRIPTNAME.username=USER,SCRIPTNAME.password=PASS TARGET_IP
sudo nmap --script-updatedb
Tcpdump Traffic Capture
Bash
sudo tcpdump -D
sudo tcpdump -i eth0
sudo tcpdump -i eth0 -nn
sudo tcpdump -i eth0 -X
sudo tcpdump -i eth0 -w FILENAME.pcap
sudo tcpdump -r FILENAME.pcap
sudo tcpdump -i eth0 host IP
sudo tcpdump -i eth0 port 443
sudo tcpdump -i eth0 portrange 1-1024
Wireshark & Tshark Filters
Bash
ip.src == IP
ip.dst == IP
http.request.method == "GET"
http.host contains "example.com"
tls.handshake.extensions_server_name contains "youtube"
dns.qry.name contains "youtube"
sudo tshark -r FILENAME.pcap
Web Enumeration & Remote Access
Bash
gobuster dir -u http://WEBNAME:PORT -w /usr/share/wordlists/dirbuster/directory-list-1.0.txt
xfreerdp /v:CLIENTIP /u:USERNAME /p:"PASSWORD"

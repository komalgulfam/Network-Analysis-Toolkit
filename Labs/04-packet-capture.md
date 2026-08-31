
# Lab 04 - Traffic Capturing with Tcpdump

## Objective
Capture live network traffic, inspect raw packets, and apply protocol filters using Tcpdump.

## Environment
- Operating System: Kali Linux
- Tool: Tcpdump
- Interface: eth0

## Tasks Performed

### 1. Live Interface Monitoring
```bash
sudo tcpdump -i eth0 -nn
Result

Captured real-time traffic on the interface with name resolution disabled.

2. Saving Capture to File
Bash
sudo tcpdump -i eth0 -w traffic.pcap
Result

Stored raw packet data into a .pcap file for later analysis.

3. Protocol and Port Filtering
Bash
sudo tcpdump -i eth0 tcp port 443
Result

Filtered output to display only secure HTTPS web traffic.

4. Reading Saved Captures
Bash
sudo tcpdump -r traffic.pcap icmp
Result

Filtered saved packet capture files specifically for ICMP traffic.

Commands Used
tcpdump -i

tcpdump -w

tcpdump -r

tcpdump portrange

What I Learned
How to capture interface traffic seamlessly.

Writing filter expressions for specific protocols and ports.

Saving and reviewing packet capture files via CLI.

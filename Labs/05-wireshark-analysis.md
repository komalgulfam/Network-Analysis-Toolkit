
# Lab 05 - Packet Analysis with Wireshark

## Objective
Analyze captured network traffic visually using Wireshark display filters.

## Environment
- Operating System: Kali Linux
- Tool: Wireshark
- File: Capture dumps

## Tasks Performed

### 1. GUI Initialization
```bash
xhost +local:root
sudo wireshark /tmp/capture.pcap &
Result

Opened Wireshark graphical interface with root permissions to inspect capture files.

2. HTTP Method Filtering
Markdown
http.request.method == "GET"
Result

Filtered traffic to isolate HTTP GET requests.

3. Domain and Host Matching
Markdown
http.host contains "example.com"
tls.handshake.extensions_server_name contains "youtube"
Result

Pinpointed specific web browsing domains and HTTPS SNI extensions.

Display Filters Used
ip.src == IP

http.request.method

tls.handshake.extensions_server_name

dns.qry.name

What I Learned
How to launch Wireshark securely from root.

Applying powerful display filters to narrow down web traffic.

Inspecting HTTP and TLS connection handshakes.

# Wireshark, Tshark & Additional Tools

## Tshark (CLI Packet Analyzer)
- `sudo tshark -D`: List network interfaces for tshark
- `sudo tshark -f "host IP" -w FILENAME`: Capture traffic to file via CLI
- `sudo tshark -r FILENAME`: Read saved traffic file via CLI

## Wireshark GUI Setup
- `xhost +local:root`: Grant local root permission for GUI application display
- `sudo wireshark /tmp/capture.pcap &`: Launch Wireshark and open capture file in background

## Wireshark Display Filters Cheat Sheet
| Requirement | Display Filter |
| :--- | :--- |
| HTTP Requests (GET Method) | `http.request.method == "GET"` |
| HTTP Domain Match | `http.host contains "example.com"` |
| HTTPS Domain Match (YouTube/Google) | `tls.handshake.extensions_server_name contains "youtube"` |
| DNS Request Match | `dns.qry.name contains "youtube"` |
| Source IP Filter | `ip.src == IP_ADDRESS` |
| Destination IP Filter | `ip.dst == IP_ADDRESS` |

## Additional Utility
- `xfreerdp /v:CLIENTIP /U:USERNAME /p:"PASSWORD"`: Connect to a remote machine via RDP

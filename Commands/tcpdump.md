# Tcpdump Cheat Sheet

This file contains network packet capture and filtering syntax using `tcpdump`.

## Interface & Basic Capture
- `sudo tcpdump -D`: List available network interfaces
- `sudo tcpdump -i eth0`: Capture traffic on eth0 interface
- `sudo tcpdump -i eth0 -nn`: Capture traffic without resolving hostnames or ports
- `sudo tcpdump -i eth0 -e`: Show link-level (MAC) headers
- `sudo tcpdump -i eth0 -X`: Display packet payload in Hex and ASCII
- `sudo tcpdump -i eth0 -XX`: Display link-level header along with Hex/ASCII
- `sudo tcpdump -i eth0 -c 10`: Capture only 10 packets then stop
- `sudo tcpdump -i eth0 -w FILENAME.pcap`: Save captured traffic to a pcap file
- `sudo tcpdump -r FILENAME.pcap`: Read saved packets from a pcap file
- `sudo tcpdump -i eth0 -nnvXX`: Capture with verbose output, no name resolution, and hex view

## Protocol & Port Filtering
- `sudo tcpdump -i eth0 host IP`: Capture traffic for a specific host
- `sudo tcpdump -i eth0 src host IP`: Filter source traffic of an IP
- `sudo tcpdump -i eth0 dest host IP`: Filter destination traffic of an IP
- `sudo tcpdump -i eth0 net 192.168.1.0/24`: Filter traffic within a network range
- `sudo tcpdump -i eth0 proto 17` (or `proto udp`): Filter UDP traffic (Protocol ID: 17)
- `sudo tcpdump -i eth0 proto 6` (or `proto tcp`): Filter TCP traffic (Protocol ID: 6)
- `sudo tcpdump -i eth0 proto 1` (or `icmp`): Filter ICMP traffic (Protocol ID: 1)
- `sudo tcpdump -i eth0 port 443`: Filter specific port traffic
- `sudo tcpdump -i eth0 tcp src port 80`: Filter TCP source port 80
- `sudo tcpdump -i eth0 portrange 1-1024`: Filter a range of ports

## Advanced Expressions & Operators
- `sudo tcpdump -i eth0 tcp and port 80`: Match multiple conditions using `and`
- `sudo tcpdump -i eth0 not icmp`: Exclude specific traffic (using `not` or `!`)
- `sudo tcpdump -i eth0 less 64`: Capture packets smaller than 64 bytes
- `sudo tcpdump -i eth0 greater 500`: Capture packets larger than 500 bytes
- `sudo tcpdump -A -r FILENAME.pcap`: Print packet payloads in ASCII text format
- `sudo tcpdump -Ar file.pcap -l | grep 'mailto'`: Parse captured stream line-by-line using grep
- `sudo tcpdump -i eth0 'tcp[13] & 2 != 0'`: Capture raw TCP SYN packets (flag analysis)

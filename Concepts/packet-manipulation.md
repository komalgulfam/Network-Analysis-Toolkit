# Packet Manipulation & Evasion Concepts

## Packet Control Options
- `-f`: Send fragmented packets to bypass simple packet filters/firewalls.
- `-Pn`: Do not skip port scanning even if host discovery shows no response.
- `--mtu NUM`: Set custom Maximum Transmission Unit size (must be a multiple of 8).
- `--scan-delay TIMEms`: Add a time delay between sent packets to avoid detection.
- `--badsum`: Send packets with an intentionally incorrect checksum to test firewall/IDS responses.

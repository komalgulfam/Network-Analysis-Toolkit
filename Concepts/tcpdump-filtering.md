# Tcpdump Packet Filtering & Analysis Concepts

## Protocol IDs & Filtering
- TCP Protocol ID = `6`
- UDP Protocol ID = `17`
- ICMP Protocol ID = `1`

## Advanced Filtering Rules
- **Port Ranges:** Use `portrange 1-1024` to capture traffic across a range of ports.
- **Multiple Conditions:** Use logical operators like `and` (e.g., `tcp and port 80`) to ensure all conditions match.
- **Exclusions:** Use `not` or `!` to exclude specific traffic (e.g., `not icmp`).
- **Packet Length:** Use `less 64` or `greater 500` to filter packets based on byte size.
- **Bitwise Flag Analysis:** Use expressions like `'tcp[13] & 2 != 0'` to filter raw packets where the SYN flag bit is active.

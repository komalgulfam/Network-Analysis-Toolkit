
# Lab 03 - Nmap Scripting Engine (NSE)

## Objective
Explore, search, and execute Nmap NSE scripts for service enumeration and vulnerability checking.

## Environment
- Operating System: Kali Linux
- Tool: Nmap & Grep
- Location: `/usr/share/nmap/scripts/`

## Tasks Performed

### 1. Finding Scripts with Grep
```bash
grep -l 'ftp.*vuln' /usr/share/nmap/scripts/*.nse
Result

Filtered script files related to FTP vulnerabilities.

2. Running Script Categories
Bash
nmap --script=default TARGET_IP
Result

Executed standard safe default scripts against target services.

3. Supplying Script Arguments
Bash
nmap --script ftp-brute --script-args ftp-brute.userfile=users.txt TARGET_IP
Result

Provided custom parameters required by specific brute-force scripts.

4. Updating Script Database
Bash
sudo nmap --script-updatedb
Result

Refreshed the Nmap script database after adding custom .nse scripts.

Commands Used
grep

nmap --script

nmap --script-args

nmap --script-updatedb

What I Learned
How to navigate the local Nmap script repository.

Executing category-specific scripts.

Passing necessary arguments to complex NSE scripts.

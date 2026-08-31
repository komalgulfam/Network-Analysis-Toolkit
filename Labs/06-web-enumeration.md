# Lab 06 - Web Enumeration with Gobuster

## Objective
Perform web directory and file discovery against target web servers.

## Environment
- Operating System: Kali Linux
- Tool: Gobuster
- Wordlist: Dirbuster lists

## Tasks Performed

### 1. Directory Scanning
```bash
gobuster dir -u http://TARGET_IP:PORT -w /usr/share/wordlists/dirbuster/directory-list-1.0.txt
Result

Enumerated hidden directories, admin panels, and resource files on the target web server.

Commands Used
gobuster dir

What I Learned
How to use wordlists for directory brute-forcing.

Identifying hidden web application endpoints.

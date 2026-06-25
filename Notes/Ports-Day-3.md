# Ports - Day 3

Summary

Common TCP/UDP ports, how to discover open services, and basic port security concepts.

Common ports
- 20/21: FTP
- 22: SSH
- 23: Telnet
- 25: SMTP
- 53: DNS
- 67/68: DHCP
- 80: HTTP
- 110: POP3
- 143: IMAP
- 443: HTTPS
- 3306: MySQL
- 3389: RDP

Tools & commands
- netstat / ss — list listening ports and connections
- lsof -i -Pn — show processes using network sockets
- nmap — port scanning and service detection

Security notes
- Minimize exposed services; use firewalls and access controls
- Move management services off standard ports only as defense-in-depth (not a sole control)

# TCP/IP Basics

Overview

This note covers core TCP/IP concepts you should know as a networking and cybersecurity practitioner. It maps the TCP/IP model to the OSI model, explains addressing and key protocols, and includes quick diagnostics and a small lab.

Learning objectives

- Understand the TCP/IP layer model and how it maps to OSI
- Know IPv4/IPv6 fundamentals and addressing concepts
- Know the difference between TCP and UDP and when each is used
- Use basic diagnostic tools: ping, traceroute, tcpdump/wireshark

TCP/IP model (conceptual mapping)

- Link / Network Interface (OSI: Physical + Data Link) — Ethernet, ARP
- Internet (OSI: Network) — IP (IPv4/IPv6), ICMP
- Transport (OSI: Transport) — TCP, UDP
- Application (OSI: Session/Presentation/Application) — HTTP, DNS, DHCP, SMTP, etc.

IP addressing basics

- IPv4: 32-bit addresses, dotted decimal (e.g., 192.0.2.1). Subnetting uses masks (/24, /16).
- IPv6: 128-bit addresses, hex colon format (e.g., 2001:db8::1). Designed for huge address space and simplified header.
- Private vs public: RFC1918 ranges for IPv4 (10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16).
- ARP resolves IPv4 addresses to MAC addresses on a LAN; Neighbor Discovery (NDP) is the IPv6 equivalent.

Transport protocols

- TCP: connection-oriented, reliable, ordered delivery. Key concepts: three-way handshake (SYN, SYN-ACK, ACK), sequence and acknowledgment numbers, flags (SYN, ACK, FIN, RST), retransmissions, congestion control.
- UDP: connectionless, low overhead, no retransmission guarantees. Common for DNS, streaming, some real-time protocols.

Common protocols and ports

- DNS (53/UDP primarily), DHCP (67/68), HTTP (80), HTTPS (443), SSH (22), SMTP (25), SNMP (161), NTP (123).

Diagnostics & tools

- ping — ICMP echo for basic reachability
- traceroute / tracert — path and per-hop latency
- arp -a / ip neigh — check ARP / neighbor cache
- ss / netstat — list sockets and listening ports
- tcpdump / tshark / Wireshark — capture and inspect packets
- nmap — port/service scanning and fingerprinting

Short labs

1) Capture a TCP three-way handshake:
   - Start a packet capture (tcpdump -i <iface> tcp and host <target>)
   - Initiate an SSH or HTTP connection and observe SYN, SYN-ACK, ACK
2) Compare TCP vs UDP flows:
   - Perform an HTTP request and a DNS lookup while capturing; note TCP setup vs single UDP query
3) Subnetting practice:
   - Given 192.168.10.0/24, split into four equal subnets and calculate ranges and broadcast addresses

Further reading

- RFC 791 (IPv4), RFC 8200 (IPv6), RFC 793 (TCP)
- “TCP/IP Illustrated, Volume 1” by W. Richard Stevens


# TCP/IP - Day 2

Summary

This note covers the TCP/IP model, key protocols, and differences vs the OSI model.

TCP/IP Layers (conceptual)
- Link/Network Interface
- Internet (IP)
- Transport (TCP, UDP)
- Application (HTTP, DNS, SMTP, etc.)

Key protocols
- IP (IPv4/IPv6) — addressing & routing
- TCP — reliable, ordered byte stream, three-way handshake
- UDP — connectionless, low overhead, used for DNS, streaming
- ICMP — diagnostics (ping)

Troubleshooting tips
- Use ping (ICMP) to check reachability
- Use traceroute/tracert to discover path and latency
- Capture traffic with tcpdump/wireshark to inspect headers

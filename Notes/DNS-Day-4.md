# DNS - Day 4

Summary

DNS fundamentals: how name resolution works, common DNS record types, and useful troubleshooting techniques.

Resolution flow
1. Client checks local cache
2. Query sent to recursive resolver (ISP or public resolver)
3. Resolver queries root, TLD, then authoritative name servers
4. Resolver returns answer to client

Common record types
- A / AAAA — IPv4 / IPv6 address records
- CNAME — canonical name (alias)
- MX — mail exchange
- NS — authoritative name servers
- TXT — arbitrary text (e.g., SPF, verification)

Tools
- dig, nslookup — query DNS records
- host — simple lookups

Security
- DNS spoofing/cache poisoning — mitigations: DNSSEC, use of authenticated resolvers
- Monitor unexpected changes to critical records

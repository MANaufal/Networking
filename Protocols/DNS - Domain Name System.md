- Converts **domain names** into **IP addresses**
- A DNS server IP is necessary for a host to have internet connectivity (usually assigned via [[DHCP - Dynamic Host Configuration Protocol|DHCP]])
- **Port 53** — UDP for queries, TCP for zone transfers / large responses
- Hierarchical structure: **Root** → **TLD** (.com, .org) → **Authoritative** (example.com)
- Common record types:
	- **A** — maps name → IPv4 address
	- **AAAA** — maps name → IPv6 address
	- **CNAME** — alias to another name
	- **MX** — mail server for the domain
	- **PTR** — reverse lookup (IP → name)
- Results are **cached** by hosts and resolvers to speed up future lookups

**Example:** Host visits `example.com`.
1. Host asks DNS server: *"What is example.com?"*
2. Server replies: `93.184.216.34`
3. Host caches the result and connects to the IP

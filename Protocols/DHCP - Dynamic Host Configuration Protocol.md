- Automatically provides IP configuration to hosts joining a network
- Assigns: **IP address, Subnet Mask, Default Gateway, DNS server**
- **UDP** — Port 67 (server), Port 68 (client)
- Leases are **temporary** — clients must renew before expiry
- Assignment process: **DORA**
	1. **Discover** — client broadcasts to find a DHCP server
	2. **Offer** — server offers an IP configuration
	3. **Request** — client requests the offered config
	4. **Acknowledge** — server confirms, lease begins

**Example:** A new laptop joins the network.
1. Laptop broadcasts a DHCP Discover
2. Server replies via DORA → laptop receives `192.168.1.50/24`, gateway `192.168.1.1`, DNS `8.8.8.8`

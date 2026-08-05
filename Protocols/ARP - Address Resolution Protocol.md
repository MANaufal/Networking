***RFC 826***

>**Directly Connected**
>1. Host A must know Host B's IP address
>2. Host A does **NOT** know Host B's MAC address
>3. Host A must use **Address Resolution Protocol (ARP)**
>4. **ARP** broadcasts a request to all MAC addresses via L2 (Layer 2)
>5. Every device has an ARP cache of the last IP addresses they contacted
>6. Host B sends an ARP response
>7. Host A can finally attach the L2 header to data to send it to Host B
>
>>**Example:** Host A (192.168.1.10) wants to reach Host B (192.168.1.20).
>>1. A broadcasts: *"Who has 192.168.1.20? Tell 192.168.1.10"*
>>2. B replies: *"192.168.1.20 is at AA:BB:CC:DD:EE:FF"*
>>3. A caches B's MAC and forwards the frame

>**[[Routers|Router]]**
>1. Host A only needs to send an ARP to the router once
>2. Host A already knows the router's IP address — it's Host A's default gateway
>
>>**Example:** Host A (192.168.1.10/24) wants to reach Host C (10.0.0.50/24) on another network.
>>1. A sees the destination is not on its local subnet
>>2. A sends an ARP for its default gateway (192.168.1.1)
>>3. Router replies with its MAC address
>>4. A forwards the frame to the router, which routes it toward Host C

>**Router to Router**
>1. A router forwarding a packet to a next-hop router needs the next hop's MAC address
>2. If not in its ARP cache, it broadcasts an ARP request for the next hop's IP
>3. The destination IP in the packet stays **unchanged** — only the L2 (MAC) header changes per hop
>
>>**Example:** R1 (10.0.0.1) forwards a packet toward Host C (192.168.2.50); the next hop is R2 (10.0.0.2).
>>1. R1's [[Routing Table|routing table]] says: `192.168.2.0/24` via `10.0.0.2`
>>2. R1 broadcasts: *"Who has 10.0.0.2? Tell 10.0.0.1"*
>>3. R2 replies with its MAC address
>>4. R1 attaches an L2 header with R2's MAC and forwards the frame — destination IP is still `192.168.2.50`

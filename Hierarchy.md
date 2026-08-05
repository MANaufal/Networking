[[Routers]] are typically connected in a hierarchy because:
1. Easier to scale
2. More consistent connectivity

Hierarchy allows for **Route Summarization**
1. Reduces number of routes in the [[Routing Table]]
2. Default Route — the ultimate route summary: `0.0.0.0/0` — *"For everything else, go here"*

**Example:** A central router (R3) connecting two branch routers (R1, R2).

**R1's Routing Table**

| Network | Next Hop |
|---------|----------|
| 192.168.1.0/24 | directly connected |
| 0.0.0.0/0 | via R3 (10.0.0.254) |

**R2's Routing Table**

| Network | Next Hop |
|---------|----------|
| 192.168.2.0/24 | directly connected |
| 0.0.0.0/0 | via R3 (10.0.0.254) |

**R3's Routing Table**

| Network | Next Hop |
|---------|----------|
| 192.168.1.0/24 | via R1 (10.0.0.1) |
| 192.168.2.0/24 | via R2 (10.0.0.2) |
| 0.0.0.0/0 | upstream (ISP) |

R3 can advertise a summarized route `192.168.0.0/22` upstream instead of two separate /24s.

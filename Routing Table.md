>A **Routing Table** is a map stored on a [[Routers|router]] listing all the networks it knows about and how to reach them.
>- Each entry contains: **destination network, next hop, and outgoing interface**
>- The router checks this table to decide where to forward every packet

>[[Routers|Router's]] Routing Table can be populated via **Three** methods:
- Directly Connected, From the networks which are attached to the router
- Static Routes, Manually provided by an Administrator
- Dynamic Routes, Learned automatically from other routes
	- Common Dynamic Routing protocols are: **RIP, OSPF, BGP, EIGRP, IS-IS**
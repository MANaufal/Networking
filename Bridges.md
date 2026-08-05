>Sits between Hub-connected hosts

- A bridge only can have 2 ports
- **L2 (Data Link) device** — makes decisions using MAC addresses
- **Learns** which MAC addresses live on each of its two sides
- Only forwards a frame to the other side **if the destination is there** — otherwise the traffic stays local
- **Splits one collision domain into two** → fewer collisions, better performance
- A bridge with many ports = [[Switches|Switch]]
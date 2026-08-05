>[[Repeater]] with multiple ports

- **L1 (Physical) device** — works with raw bits/signals, no intelligence
- Anything received on one port is **repeated out every other port** (flooding)
- Every host hears everyone's traffic — privacy risk (easy to sniff)
- **Half-duplex** — only one device can "talk" at a time
- Creates **one big collision domain**:
	- More hosts = more collisions = slower network
	- Hosts use **CSMA/CD** to detect collisions and retry
- No MAC address table, no filtering — can't send to a specific host
- Obsolete — replaced by [[Switches]]
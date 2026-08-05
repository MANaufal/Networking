>Taking a network and dividing it into *sub-networks*

>Seven attributes of Subnetting

| Name           | Description                          |
| -------------- | ------------------------------------ |
| Network ID     | First IP address in each Sub-Network |
| Broadcast IP   | Last IP address in each Sub-Network  |
| First Host IP  | IP address *after* the Network ID    |
| Last Host IP   | IP address *before* the Broadcast IP |
| Next Network   | IP address *after* the Broadcast IP  |
| # IP Addresses | Number of IP addresses               |
| CIDR/Subnet    | Converting between CIDR/Subnet Mask  |

**Example:** All seven attributes derived from a single IPv4 address — `192.168.1.10/26`

| Name           | Value                   | How                                          |
| -------------- | ----------------------- | -------------------------------------------- |
| Network ID     | `192.168.1.0`           | First address of the block                   |
| Broadcast IP   | `192.168.1.63`          | Last address of the block                    |
| First Host IP  | `192.168.1.1`           | Network ID + 1                               |
| Last Host IP   | `192.168.1.62`          | Broadcast IP − 1                             |
| Next Network   | `192.168.1.64`          | Broadcast IP + 1                             |
| # IP Addresses | 64 (62 usable)          | 2^(32−26) = 64, minus Network ID & Broadcast |
| CIDR/Subnet    | /26 = `255.255.255.192` | 26 network bits                              |

**Working it out:**
1. `/26` → Subnet Mask `255.255.255.192` → **block size = 64** (256 − 192)
2. Blocks start at `.0`, `.64`, `.128`, `.192` → `192.168.1.10` falls in the first block: `.0`–`.63`
3. Apply the rules from the table:
	- Network ID = `.0`, Broadcast = `.63`
	- Usable hosts = `.1`–`.62` (that's the 62 usable addresses)
	- The next sub-network starts at `192.168.1.64`

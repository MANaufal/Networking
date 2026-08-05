- Transfers files between a client and a server
- Uses **two connections**:
	- **Port 21** — control connection (commands, stays open)
	- **Port 20** — data connection (actual file transfer)
- Common commands:
	- **RETR** — retrieve (download) a file
	- **STOR** — store (upload) a file
	- **LIST** — list directory contents
- **No encryption** — credentials and data sent in plaintext (use SFTP/FTPS instead)

**Example:** Client downloads a file.
1. Client → `RETR report.pdf` (over port 21)
2. Server → sends `report.pdf` (over port 20)

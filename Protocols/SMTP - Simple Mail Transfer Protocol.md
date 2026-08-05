- Used to **send** email — from client to server, and between mail servers
- **Port 25** (server-to-server relay), **Port 587** (client submission)
- **Push** protocol — it only sends mail; retrieval is done by **POP3 / IMAP**
- Basic commands:
	- **HELO** — identify the sender's server
	- **MAIL FROM** — sender address
	- **RCPT TO** — recipient address
	- **DATA** — the message itself

**Example:** alice@a.com emails bob@b.com.
1. Alice's client pushes the mail to a.com's SMTP server
2. a.com's server pushes it to b.com's server (SMTP relay)
3. Bob retrieves it later using POP3/IMAP

- Successor to [[SSL - Secure Sockets Layer|SSL]] — the current standard for encrypted communication
- Provides:
	- **Confidentiality** — symmetric encryption of the session
	- **Integrity** — hashing detects tampering
	- **Authentication** — server proves identity with a certificate
- Versions:
	- **TLS 1.2** — widely deployed
	- **TLS 1.3** — latest; faster handshake, removed weak ciphers
- Secures [[HTTPS - Secured HTTP|HTTPS]], email, VPNs, and more

**Example:** TLS handshake (simplified).
1. **Client Hello** — supported TLS versions + cipher suites
2. **Server Hello** — chosen cipher + server certificate
3. **Key exchange** — both sides derive the same session key
4. All following traffic is encrypted with the session key

- Used for communication between a client and a **web server**
- **Port 80** (HTTP), **Port 443** ([[HTTPS - Secured HTTP]] — encrypted)
- **Stateless** — every request is independent, server doesn't remember previous ones
- Common methods:
	- **GET** — retrieve a resource
	- **POST** — submit data to the server
	- **PUT / DELETE** — update / remove a resource
- Server replies with a status code:
	- **200 OK** — success
	- **404** — not found
	- **500** — server error

**Example:** Client requests a web page.
1. Client → `GET /index.html`
2. Server → `200 OK` + page content

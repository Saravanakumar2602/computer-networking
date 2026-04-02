# HTTP, Email, and DNS: Application Layer Essentials

## Introduction

The application layer is where users interact with the network. This chapter covers HTTP (web), email protocols, cookies, and DNS—the backbone of modern internet services.

---

## HTTP (Hypertext Transfer Protocol)

- **Purpose:** Foundation of data communication on the World Wide Web
- **Layer:** Application (OSI Layer 7)
- **Transport:** Uses TCP (port 80)

**HTTP Methods:**
- **GET:** Retrieve data
- **POST:** Submit data
- **PUT:** Update data
- **DELETE:** Remove data

**Status Codes:**
- 1xx: Informational
- 2xx: Success (200 OK, 201 Created)
- 3xx: Redirection (301 Moved Permanently)
- 4xx: Client Error (404 Not Found)
- 5xx: Server Error (500 Internal Server Error)

**Example:**
When you visit a website, your browser sends an HTTP GET request; the server responds with the webpage.

**Diagram:**
```
Browser --GET--> Server
	<--200 OK--
```

---

## Cookies

- **Definition:** Small text files stored by websites on your device
- **Purpose:** Remember login, preferences, shopping carts
- **Third-party cookies:** Set by domains other than the one visited (ads, analytics)

**Privacy Note:** Third-party cookies are often used for tracking and targeted advertising.

---

## Email Protocols

### 1. SMTP (Simple Mail Transfer Protocol)
- **Purpose:** Sending emails from client to server or between servers
- **Port:** 25 (unencrypted), 465/587 (encrypted)

### 2. POP3 (Post Office Protocol 3)
- **Purpose:** Downloading emails to local device, usually deletes from server
- **Port:** 110 (unencrypted), 995 (encrypted)

### 3. IMAP (Internet Message Access Protocol)
- **Purpose:** Accessing and managing emails on the server, sync across devices
- **Port:** 143 (unencrypted), 993 (encrypted)

**Email Workflow Example:**
1. User composes email in client
2. Client sends via SMTP to mail server
3. Recipient retrieves email using POP3 or IMAP

**Diagram:**
```
Sender --SMTP--> Mail Server --SMTP--> Recipient's Server
Recipient --IMAP/POP3--> Mail Server
```

---

## DNS (Domain Name System)

- **Purpose:** Translates human-readable domain names (www.example.com) to IP addresses
- **Layer:** Application (OSI Layer 7)

**How DNS Works:**
1. User enters www.example.com
2. Browser asks local DNS resolver
3. Resolver queries root DNS server
4. Root refers to TLD server (.com)
5. TLD refers to authoritative server
6. IP address returned to browser

**Diagram:**
```
User --> Resolver --> Root DNS --> TLD DNS --> Authoritative DNS --> IP
```

---

## Further Reading

- [How HTTP Works (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview)
- [How Email Works (Cloudflare)](https://www.cloudflare.com/learning/email-security/how-email-works/)
- [DNS Explained (Cloudflare)](https://www.cloudflare.com/learning/dns/what-is-dns/)

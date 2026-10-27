# HTTP vs HTTPS

## 📌 Introduction

HTTP and HTTPS are protocols used for communication between a web browser and a web server. They help users access websites and exchange information over the internet.

- **HTTP:** Hypertext Transfer Protocol
- **HTTPS:** Hypertext Transfer Protocol Secure

The main difference is that HTTPS uses encryption to protect data exchanged between the browser and the server, while HTTP does not provide this protection by itself.

## 🌐 What is HTTP?

HTTP is a protocol that allows web browsers and web servers to communicate with each other.

### Features of HTTP
- Data is transmitted without encryption by HTTP itself.
- It is generally faster in terms of security-related processing overhead, although this is rarely a meaningful advantage with modern HTTPS.
- It commonly uses port **80**.
- Data transmitted over HTTP can be intercepted or modified by attackers on an untrusted network.

### Example

```text
http://example.com
```

## 🔒 What is HTTPS?

HTTPS is the secure version of HTTP. It uses **TLS (Transport Layer Security)** to encrypt communication between the browser and the web server.

### Features of HTTPS
- Encrypts data transmitted between the browser and server.
- Helps protect sensitive information, such as passwords and payment details.
- Uses digital certificates to authenticate the server.
- Helps protect data integrity by detecting unauthorized changes during transmission.
- Commonly uses port **443**.

### Example

```text
https://example.com
```

## ⚖️ HTTP vs HTTPS: Key Differences

| Feature | HTTP | HTTPS |
|---|---|---|
| Full Form | Hypertext Transfer Protocol | Hypertext Transfer Protocol Secure |
| Security | No built-in encryption | Uses TLS encryption |
| Default Port | 80 | 443 |
| Data Encryption | No | Yes |
| Certificate | Not required | Server certificate required |
| Data Integrity | No TLS-based protection | Protected by TLS |
| Authentication | No TLS server authentication | Server authentication through certificates |
| URL | Starts with `http://` | Starts with `https://` |
| Recommended Use | Not suitable for sensitive data | Recommended for websites and APIs |

## 🔄 How HTTP and HTTPS Work

### HTTP Workflow
1. The user enters an HTTP URL in the browser.
2. The browser sends an HTTP request to the server.
3. The server processes the request.
4. The server returns an HTTP response.
5. The browser displays the requested content.

### HTTPS Workflow
1. The user enters an HTTPS URL in the browser.
2. The browser establishes a secure TLS connection with the server.
3. The server presents its digital certificate.
4. The browser validates the certificate and negotiates secure session keys.
5. The browser and server exchange encrypted HTTP requests and responses.

## 🛡️ Why is HTTPS Important?

HTTPS is important because it:

- Protects login credentials and personal information.
- Reduces the risk of data interception.
- Helps prevent unauthorized modification of data in transit.
- Verifies the identity of the website through certificate validation.
- Supports secure communication between applications and APIs.

**Note:** HTTPS protects data in transit, but it does not guarantee that a website is trustworthy or that the server itself is secure.

## 💻 HTTP vs HTTPS in Application Support

As an Application Support Engineer, understanding HTTP and HTTPS is useful for troubleshooting website and API connectivity issues.

Common troubleshooting scenarios include:

- **HTTP 400:** Bad Request
- **HTTP 401:** Unauthorized
- **HTTP 403:** Forbidden
- **HTTP 404:** Not Found
- **HTTP 500:** Internal Server Error
- **HTTP 502:** Bad Gateway
- **HTTP 503:** Service Unavailable
- **HTTP 504:** Gateway Timeout
- **SSL/TLS errors:** Certificate expiration, hostname mismatch, or trust-chain issues
- **Connection issues:** Incorrect ports, firewall restrictions, or TLS handshake failures

**Important:** HTTP status codes describe the result of an HTTP request. They are different from HTTP and HTTPS, which are communication protocols.

## 🧪 Practical Examples

### Check an HTTP URL

```bash
curl -I http://example.com
```

### Check an HTTPS URL

```bash
curl -I https://example.com
```

The `-I` option requests the response headers, which can help when investigating website and API connectivity.

### Check HTTPS Certificate Details

```bash
openssl s_client -connect example.com:443 -servername example.com
```

This command helps inspect the TLS connection and certificate information.

## ✅ Conclusion

HTTP and HTTPS are communication protocols used on the internet. HTTP does not encrypt traffic by itself, whereas HTTPS uses TLS to provide encryption, data integrity, and server authentication.

For modern websites, applications, and APIs, **HTTPS is the recommended choice** because it provides essential security for data transmitted between clients and servers.

## 📚 References

- [MDN Web Docs – HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP)
- [MDN Web Docs – Transport Layer Security (TLS)](https://developer.mozilla.org/en-US/docs/Web/Security/Transport_Layer_Security)
- [Cloudflare – What is HTTPS?](https://www.cloudflare.com/learning/ssl/what-is-https/)

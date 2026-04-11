# HTTP Basics

## What is HTTP?
**HyperText Transfer Protocol** – Application layer protocol for distributed systems. Client-server model.

## HTTP Request Structure
POST /api/users HTTP/1.1
Host: example.com
Content-Type: application/json
Authorization: Bearer abc123

{"name": "Alice"}

## Components:
1. **Request line** – Method + Path + HTTP version
2. **Headers** – Key-value metadata
3. **Body** – Optional data (POST/PUT/PATCH)

## HTTP Response Structure
HTTP/1.1 200 OK
Content-Type: application/json
Cache-Control: max-age=3600

{"id": 1, "name": "Alice"}

## URL Anatomy
https://api.github.com:443/repos/octocat/hello-world?sort=stars#readme
_/ _/ _/ _____________________/ _/ _/
| | | | | |
scheme host port path query fragment

## Common HTTP Methods

| Method | Safe | Idempotent | Has Body | Use case |
|--------|------|------------|----------|----------|
| GET    | Yes  | Yes        | No       | Read data |
| POST   | No   | No         | Yes      | Create resource |
| PUT    | No   | Yes        | Yes      | Full update |
| PATCH  | No   | No         | Yes      | Partial update |
| DELETE | No   | Yes        | Maybe    | Remove resource |
| HEAD   | Yes  | Yes        | No       | Get metadata only |
| OPTIONS| Yes  | Yes        | No       | Check allowed methods |

**Safe**: Does not change server state  
**Idempotent**: Multiple identical requests = same result

## HTTP Versions Quick Comparison

| Version | Year | Key Feature |
|---------|------|-------------|
| HTTP/1.0 | 1996 | Basic, one connection per request |
| HTTP/1.1 | 1997 | Persistent connections, pipelining |
| HTTP/2   | 2015 | Multiplexing, server push, binary |
| HTTP/3   | 2022 | QUIC (UDP-based), faster handshake |

## Hands-on: See HTTP in action

```bash
# View full request/response including headers
curl -v https://httpbin.org/get

# Save response headers only
curl -I https://google.com

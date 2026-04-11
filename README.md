# HTTP Requests Guide

> **From beginner to advanced** — Master HTTP requests, headers, status codes, authentication, and real-world debugging. Built for DevOps engineers, backend developers, and networking enthusiasts.

![GitHub repo size](https://img.shields.io/github/repo-size/yourusername/http-requests-guide)
![GitHub last commit](https://img.shields.io/github/last-commit/yourusername/http-requests-guide)
![License](https://img.shields.io/badge/license-MIT-green)

## Why this guide?

HTTP is everywhere — browsers, APIs, microservices, cloud load balancers, Kubernetes ingress, serverless functions. If you work with systems, you **must** know HTTP inside out.

This guide gives you:
- Clear explanations with real-world scenarios
- Copy-paste ready examples (curl, JavaScript, Python)
- Troubleshooting tips for DevOps
- Interview Q&A to help you get hired

## What's inside

| File | Topic |
|------|-------|
| [01-http-basics.md](01-http-basics.md) | HTTP protocol structure, URLs, methods overview |
| [02-get-requests.md](02-get-requests.md) | GET – query params, caching, idempotency |
| [03-post-requests.md](03-post-requests.md) | POST – creating resources, request body, safety |
| [04-put-vs-patch.md](04-put-vs-patch.md) | PUT (full update) vs PATCH (partial update) |
| [05-delete-requests.md](05-delete-requests.md) | DELETE, idempotency, soft delete patterns |
| [06-head-options.md](06-head-options.md) | HEAD (metadata only), OPTIONS (CORS preflight) |
| [07-http-headers-deep-dive.md](07-http-headers-deep-dive.md) | 30+ critical headers (Content-Type, Auth, Cache, CORS) |
| [08-status-codes-guide.md](08-status-codes-guide.md) | 1xx,2xx,3xx,4xx,5xx – when they happen & how to fix |
| [09-authentication-methods.md](09-authentication-methods.md) | Basic, Bearer, JWT, API Keys, OAuth2 flows |
| [10-realworld-examples.md](10-realworld-examples.md) | GitHub API, Stripe, AWS S3, Docker Registry |
| [11-rest-api-vs-graphql.md](11-rest-api-vs-graphql.md) | Compare HTTP styles |
| [12-http2-vs-http3.md](12-http2-vs-http3.md) | Performance, multiplexing, QUIC |
| [13-troubleshooting-tools.md](13-troubleshooting-tools.md) | curl, wget, Postman, Wireshark, tcpdump, mitmproxy |
| [14-interview-questions.md](14-interview-questions.md) | 40+ real HTTP questions asked at FAANG & startups |

## Quick examples

# GET request with curl
```js
curl -X GET "https://api.github.com/users/octocat" -H "Accept: application/json"
```
# POST request
curl -X POST "https://httpbin.org/post" \
  -H "Content-Type: application/json" \
  -d '{"name":"HTTP Guide"}'
  
# Try it yourself
## Use these free test APIs:

- httpbin.org – Echo server for testing
- jsonplaceholder.typicode.com – Fake REST API
- reqres.in – Mock API for testing

# Who this is for
## Role	Why it matters
- Backend dev	Design APIs, debug integrations
- DevOps/SRE	Debug nginx, load balancers, API gateways
- Frontend dev	Understand fetch/XHR, CORS, caching
- Networking	Protocol deep dive

# HTTP Requests Guide

A simple guide to understanding HTTP requests for beginners.

## What you'll learn

- What is HTTP and how it works
- GET, POST, PUT, PATCH, DELETE methods
- HTTP headers and status codes
- Authentication (tokens, API keys)
- Real-world examples

## Contents

| File | Topic |
|------|-------|
| [01-basics.md](01-basics.md) | HTTP basics - what is a request/response |
| [02-get-post.md](02-get-post.md) | GET and POST methods with examples |
| [03-put-patch-delete.md](03-put-patch-delete.md) | PUT, PATCH, DELETE explained |
| [04-headers-status.md](04-headers-status.md) | Headers and status codes cheat sheet |
| [05-authentication.md](05-authentication.md) | How to prove who you are |
| [06-examples.md](06-examples.md) | Real APIs you can test yourself |

## Quick Example

```bash
# GET request
curl https://api.github.com/users/octocat

# POST request
curl -X POST https://httpbin.org/post \
  -H "Content-Type: application/json" \
  -d '{"name":"Zeeshan"}'

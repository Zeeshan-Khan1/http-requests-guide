# HTTP Headers and Status Codes

## What are Headers?

Headers are like **labels on a package**. They give extra information.
Authorization: Bearer your-token
Content-Type: application/json
Accept: application/json

## Common Headers You Should Know

| Header | What it does | Example |
|--------|--------------|---------|
| `Content-Type` | What data you're sending | `application/json` |
| `Accept` | What data you want back | `application/json` |
| `Authorization` | Prove who you are | `Bearer token123` |
| `User-Agent` | What browser/app you use | `Chrome/120.0` |
| `Cookie` | Remember you | `session=abc123` |

---

## Status Codes - What the Numbers Mean

### The 5 Families

| Range | Meaning | Simple |
|-------|---------|--------|
| 1xx | Information | "Working on it" |
| 2xx | Success | "Done!" |
| 3xx | Redirect | "Go here instead" |
| 4xx | Your fault | "You made a mistake" |
| 5xx | Server's fault | "We made a mistake" |

---

### 2xx - Success (Good!)

| Code | Meaning | When |
|------|---------|------|
| 200 OK | Everything worked | GET success |
| 201 Created | Made something new | POST success |
| 204 No Content | Worked, nothing to return | DELETE success |

---

### 4xx - Your Mistake (Fix these!)

| Code | Meaning | What to do |
|------|---------|------------|
| 400 Bad Request | Your data is wrong | Check your JSON |
| 401 Unauthorized | You're not logged in | Add your token |
| 403 Forbidden | You don't have permission | Get access first |
| 404 Not Found | Wrong URL | Check the address |
| 429 Too Many Requests | You're spamming | Slow down! |

---

### 5xx - Their Mistake (Not your problem!)

| Code | Meaning | What to do |
|------|---------|------------|
| 500 Internal Error | Server crashed | Try again later |
| 502 Bad Gateway | Server got bad response | Their problem |
| 503 Unavailable | Server too busy | Wait and retry |
| 504 Timeout | Server took too long | Try again |

---

## Status Code Cheat Sheet

| Code | Meaning |
|------|---------|
| 200 | "Yes, here's your data" |
| 201 | "Yes, I created it" |
| 400 | "You sent bad data" |
| 401 | "Login first" |
| 403 | "You're not allowed" |
| 404 | "Doesn't exist" |
| 500 | "Server broke (their fault)" |

---

## See Headers in Action

# See only headers
```
curl -I https://google.com
```
# See everything (headers + body)
```
curl -v https://google.com
```
## Quick Memory Tip

| Code Range | Remember As |
|------------|-------------|
| 2xx | 2 good (Success) |
| 3xx | 3 go somewhere else (Redirect) |
| 4xx | 4 your fault (Client error) |
| 5xx | 5 server's fault (Server error) |

# HTTP Basics - Simple Explanation

## What is HTTP?

HTTP is how computers talk to each other on the internet.

When you open a website, your computer sends an **HTTP request** to a server. The server sends back an **HTTP response**.

## Simple Analogy

| Real World | HTTP |
|------------|------|
| You | Client (your computer) |
| Calling a restaurant | HTTP Request |
| Restaurant kitchen | Server |
| They bring you food | HTTP Response |
# Save response headers only
curl -I https://google.com
## Parts of an HTTP Request
GET /users/123 HTTP/1.1
Host: api.example.com
Content-Type: application/json

{"name": "Zeeshan"}

text

| Part | What it means |
|------|---------------|
| GET | The action (what do you want to do?) |
| /users/123 | The resource (what are you asking for?) |
| Host | Which server? |
| Content-Type | What kind of data are you sending? |
| Body | The actual data (for POST/PUT/PATCH) |

## Parts of an HTTP Response
HTTP/1.1 200 OK
Content-Type: application/json

{"id": 123, "name": "Zeeshan"}

text

| Part | What it means |
|------|---------------|
| 200 | Status code (everything worked) |
| OK | Status message |
| Content-Type | What kind of data is coming back |
| Body | The actual data |

## HTTP Methods at a Glance

| Method | Action | Changes anything? |
|--------|--------|-------------------|
| GET | Read | No |
| POST | Create | Yes |
| PUT | Replace all | Yes |
| PATCH | Update part | Yes |
| DELETE | Remove | Yes |

## Try It Yourself

Open terminal and run:

```bash
curl https://httpbin.org/get

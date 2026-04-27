# PUT, PATCH, and DELETE - Updating and Removing

## PUT - Replace Everything

PUT replaces an entire resource. Think of it like **overwriting a whole file**.

### Example

```bash
curl -X PUT https://jsonplaceholder.typicode.com/posts/1 \
  -H "Content-Type: application/json" \
  -d '{"id":1,"title":"New Title","body":"New Body","userId":1}'
  ```
### Important
You must send ALL fields. Missing fields get deleted!

### PUT Analogy
Imagine a form with 3 fields: Name, Email, Age

### What you send	Result
```
{"email": "new@email.com"}	Name and Age disappear!
{"name": "Zeeshan", "email": "new@email.com", "age": 22}	All fields updated correctly
PATCH - Update One Thing
PATCH only updates what you send. Think of it like editing just one line of a file.
```
### Example
```
curl -X PATCH https://jsonplaceholder.typicode.com/posts/1 \
  -H "Content-Type: application/json" \
  -d '{"title":"Only change this field"}'
  ```
### Important
Other fields stay exactly the same. Nothing gets deleted!

## PUT vs PATCH - Quick Comparison

| | PUT | PATCH |
|-|-----|-------|
| **What it does** | Replace everything | Update only what you send |
| **Need all fields?** | Yes | No |
| **Safe for partial updates?** | No (dangerous!) | Yes |
| **When to use** | You have the complete data | You only have changes |
| **Analogy** | Replace entire file | Edit one line |

## Simple Rule

| If you have... | Use... |
|----------------|--------|
| The ENTIRE object | PUT |
| Just the changes | PATCH |

## DELETE - Remove Data

DELETE removes a resource. Think of it like **throwing something away**.

### Example

```bash
curl -X DELETE https://jsonplaceholder.typicode.com/posts/1
curl -X DELETE https://jsonplaceholder.typicode.com/posts/1
```
## What you get back

| Response Code | Meaning |
|---------------|---------|
| 200 OK | Deleted, here's what was deleted |
| 204 No Content | Deleted successfully, nothing to return |
| 404 Not Found | Already deleted or doesn't exist |

## Two Types of Delete

| Type | What happens | Recoverable? | Example |
|------|--------------|--------------|---------|
| Hard Delete | Gone forever | No | Deleting a tweet permanently |
| Soft Delete | Marked as deleted | Yes | Moving to trash folder |

## Soft Delete Example

Instead of actually deleting, you mark it as deleted:

```bash
PATCH /users/123
{"status": "deleted"}

PATCH /users/123
{"status": "deleted"}
```
### The data still exists in the database, just hidden from users.

Complete Example - Managing a User
bash
# Create a user (POST)
curl -X POST https://api.example.com/users \
  -d '{"name":"Zeeshan","email":"z@example.com"}'

# Read user (GET)
curl https://api.example.com/users/123

# Update entire user (PUT)
curl -X PUT https://api.example.com/users/123 \
  -d '{"name":"Zeeshan Khan","email":"new@example.com","age":23}'

# Update just email (PATCH)
curl -X PATCH https://api.example.com/users/123 \
  -d '{"email":"updated@example.com"}'

# Delete user (DELETE)
curl -X DELETE https://api.example.com/users/12

# GET and POST - The Most Common Methods

## GET - Reading Data

GET is for **getting** information. It never changes anything.

### Example

```bash
curl https://api.github.com/users/octocat
```
### This gets GitHub user "octocat" profile.

- When you use GET every day
- What you do	The GET request
- Go to YouTube	GET youtube.com
- Search "cats"	GET youtube.com/results?q=cats
- Check weather	GET weather.com/lahore
- GET with Parameters

### POST - Creating Data
POST is for creating new things.

### Example
```bash
curl -X POST https://jsonplaceholder.typicode.com/posts \
  -H "Content-Type: application/json" \
  -d '{"title":"My Post","body":"Hello World"}'
```
This creates a new post.

When you use POST every day
What you do	POST request
Sign up for Instagram	POST your info to Instagram
Post a tweet	POST your message to Twitter
Add to cart	POST product to your cart
GET vs POST - Quick Comparison
GET	POST
Purpose	Read data	Create data
Changes server?	No	Yes
Data location	In the URL	In the body (hidden)
Can bookmark?	Yes	No
Size limit	~2000 characters	Much larger
Use for	Search, view pages	Forms, signup, uploads
Important!
GET is safe to click multiple times

POST will create duplicate data if clicked twice

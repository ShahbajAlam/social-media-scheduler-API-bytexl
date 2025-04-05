## API Documentation

**Base URL**: https://jcd5sf-3000.bytexl.dev

---

#### 1. Get All Posts

- **URL**: https://jcd5sf-3000.bytexl.dev/api/posts
- **Method**: GET
- **Auth required**: No
- **Query params**: None
- **Response**
```
[
  {
    "_id": "string",
    "title": "string",
    "content": "string",
    "scheduledFor": "ISODate",
    "platforms": ["string"],
    "image": "string"
  }
]
```
---

#### 2. Create a New Post

- **URL**: https://jcd5sf-3000.bytexl.dev/api/posts
- **Method**: POST
- **Auth required**: No
- **Headers**: "Content-Type: application/json"
- **Request Body**:
```
{
  "title": "string",
  "content": "string",
  "scheduledFor": "ISODate",
  "platforms": ["string"],
  "image": "string (optional)"
}
```
- **Response (OK):**
```
{
  "message": "Post created successfully",
  "post": {
    "_id": "string",
    "title": "string",
    "content": "string",
    "scheduledFor": "ISODate",
    "platforms": ["string"],
    "image": "string"
  }
}
```
- **Response (Error):**
```
{
  "error": "All fields are required"
}
    or,
{
  "error": "Failed to create post"
}
```
---

#### 3. Delete Post by ID

- **URL**: https://jcd5sf-3000.bytexl.dev/api/posts/:id
- **Method**: DELETE
- **Auth required**: No
- **Params**: id (string) 
- **Response (OK):**
```
{
  "message": "Post deleted successfully"
}
```
- **Response (Error):**
```
{
  "error": "Post not found"
}
    or,
{
  "error": "Failed to delete post"
}
```

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

- **Example response**
```
[
  {
    "_id": "67da9112c9b2faa1e2b40c29",
    "title": "Cover Picture",
    "content": "Update the cover picture",
    "scheduledFor": "Wed Mar 19 2025 10:45:00 GMT+0000 (Coordinated Universal Time)",
    "platforms": ["facebook"],
    "image": "data:image/png;base64, ....
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

- **Example response**
```
{
  "message": "Post created successfully",
  "post": {
    "title": "Reel",
    "content": "Share a reel",
    "scheduledFor": "Wed Mar 19 2025 10:45:00 GMT+0000 (Coordinated Universal Time)",
    "platforms": ["instagram"],
    "image": "data:image/png;base64, ...
    "_id": "67f10d2469aa78e2b0529423",
    "__v": 0
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

- **Example response**
```
{
  "message": "Post deleted successfully"
}
```

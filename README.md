# Todo
Golang todo rest server

# Endpoints
## POST /sign-up
Create new user by JWT

**Request:**
```
{
    "name": "name",
    "username": "username",
    "password": "password"
}
```
**Response:**
```
{
    "id": "1"
}
```
## POST /sign-in
Sign in

**Request:**
```
{
    "username": "username",
    "password": "password"
}
```
**Response:**
```
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE1NjA5NjMyMjUsImlhdCI6MTU2MDg3NjgyNSwidXNlcl9pZCI6IjVkMDkxNzE2ZGI4MjEyZTFhMmVmYjMzYSIsInVzZXJuYW1lIjoibmV3dXNlciIsInBhc3N3b3JkIjoiXHVmZmZkXHVmZmZkJ1x1MDAxMlx1ZmZmZFx1ZmZmZEBcdWZmZmRcdTAwMTJRXHVmZmZkXHVmZmZkYdWt3qVv25oifQ.eruNfiyxFSm3H1s4uleY9Cuxw-D6qbjukjwI1kTwn70"
}
```
***Note: All *api* endpoints requires Bearer token authentication**
## POST /api/lists
Create new todo list

**Request:**
```
{
    "title": "title",
    "description": "description"
}
```
**Response:**
```
{
    "id": "1"
}
```
## GET /api/lists
Return todo lists

**Response:**
```
[
    {
        "id": "1",
        "title": "justtitle1",
        "description": "description"
    },
    {
        "id": "2",
        "title": "justtitle2",
        "description": "description"
    }
]
```
## GET /api/lists/{id}
Return todo list info

**Response:**
```
{
    "id": "1",
    "title": "justtitle1",
    "description": "description"
}
```
## PUT /api/lists/{id}
Update todo list

**Request:**
```
{
    "title": "justtitle1",
    "description": "description"
}
```
**Response:**
```
{
    "status": "ok"
}
```
## DELETE /api/lists/{id}
Delete chat

**Response:**
```
{
    "status": "ok"
}
```
## POST /api/lists/{id}/items
Create new list's item

**Request:**
```
{
    "title": "justtitle1",
    "description": "description",
    "done": "false"
}
```
**Response:**
```
{
    "id": "1"
}
```
## GET /api/lists/{id}/items
Return list's items

**Response:**
```
[
    {
        "id": "1",
        "title": "justtitle1",
        "description": "description",
        "done": "true"
    },
    {
        "id": "2",
        "title": "justtitle2",
        "description": "description",
        "done": "false"
    }
]
```
## GET /api/items/{id}
Return item info

**Response:**
```
{
    "id": "1",
    "title": "justtitle1",
    "description": "description",
    "done": "true"
}
```
## PUT /api/items/{id}
Update item info

**Request:**
```
{
    "title": "justtitle1",
    "description": "description",
    "done": "false"
}
```
**Response:**
```
{
    "status": "ok"
}
```
## DELETE /api/items/{id}
Delete item

**Response:**
```
{
    "status": "ok"
}
```
# Run
To run local project:
`go run main.go`

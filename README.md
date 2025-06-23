
---

```markdown
# 🗂️ MongoDB + Golang REST API

A simple CRUD API in Go using MongoDB as the database, built with the `mgo` driver and `httprouter`.

## 📦 Project Structure

```

mongo-golang/
├── controllers/
│   └── user.go       # Handles HTTP endpoints
├── models/
│   └── user.go       # User struct model
├── main.go           # App entry point and route setup

````

---

## 🚀 Features

- 🔎 Get user by ID
- ➕ Create user
- ❌ Delete user
- Uses MongoDB for persistent storage
- Clean MVC-like structure

---

## ⚙️ Requirements

- [Go](https://golang.org/dl/) 1.16 or higher
- [MongoDB](https://www.mongodb.com/try/download/community) (running locally on port `27017`)

---

## 🛠️ Installation

1. Clone the repo:

```bash
git clone https://github.com/yourusername/mongo-golang.git
cd mongo-golang
````

2. Install dependencies:

```bash
go mod tidy
```

3. Start MongoDB (make sure it's running on `localhost:27017`):

```bash
net start MongoDB     # Windows
# or
sudo systemctl start mongod   # Linux
# or
brew services start mongodb-community@6.0  # macOS
```

4. Run the app:

```bash
go run main.go
```

Your API will be live at `http://localhost:9000`

---

## 📬 API Endpoints

### 🔹 Create User

```
POST /user
```

#### Request Body (JSON):

```json
{
  "name": "Alice",
  "gender": "Female",
  "age": 30
}
```

---

### 🔹 Get User by ID

```
GET /user/:id
```

#### Example:

```
GET /user/64a1f01f6cbf3a5c9e2a2123
```

---

### 🔹 Delete User

```
DELETE /user/:id
```

#### Example:

```
DELETE /user/64a1f01f6cbf3a5c9e2a2123
```

---

## 🧠 Notes

* Make sure MongoDB is running **before** starting the Go server.
* MongoDB will create the `mongo-golang` database and `users` collection on the fly.

---

## 📌 License

This project is open source and available under the [MIT License](LICENSE).

```

---

Let me know if you'd like me to add:

- `curl` or Postman test commands  
- Docker support  
- Swagger/OpenAPI documentation  
- Update instructions for `go.mongodb.org/mongo-driver` (the newer Mongo driver)
```

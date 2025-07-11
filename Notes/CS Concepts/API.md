### What is a REST API?

**REST (Representational State Transfer)** is a standard architecture for designing APIs using **HTTP methods** to manage resources (like users, posts, items).

---

### 🚦 Key HTTP Methods

| Method   | Purpose        | Example Action          |
| -------- | -------------- | ----------------------- |
| `GET`    | Read data      | Get a list or item      |
| `POST`   | Create data    | Add a new item          |
| `PUT`    | Update/replace | Modify an existing item |
| `DELETE` | Delete data    | Remove an item          |

---

## 🏗️ Basic Flask REST API Template

```python
from flask import Flask, jsonify, request

app = Flask(__name__)

# Sample in-memory data (mock database)
books = [
    {"id": 1, "title": "The Alchemist", "author": "Paulo Coelho"},
    {"id": 2, "title": "1984", "author": "George Orwell"},
]
```

---

## 🚀 1. **GET** – Fetch All Items

```python
@app.route("/api/books", methods=["GET"])
def get_books():
    return jsonify(books)
```

🧪 Test in Postman:
**GET** → `http://127.0.0.1:5000/api/books`

---

## 🔍 2. **GET** – Fetch One Item by ID

```python
@app.route("/api/books/<int:book_id>", methods=["GET"])
def get_book(book_id):
    for book in books:
        if book["id"] == book_id:
            return jsonify(book)
    return jsonify({"error": "Book not found"}), 404
```

🧪 Example:
**GET** → `http://127.0.0.1:5000/api/books/2`

---

## ➕ 3. **POST** – Add a New Item

```python
@app.route("/api/books", methods=["POST"])
def add_book():
    data = request.get_json()
    new_book = {
        "id": len(books) + 1,
        "title": data["title"],
        "author": data["author"]
    }
    books.append(new_book)
    return jsonify(new_book), 201
```

🧪 Example in Postman:
**POST** → `http://127.0.0.1:5000/api/books`
**Body (raw JSON)**:

```json
{
  "title": "Sapiens",
  "author": "Yuval Noah Harari"
}
```

---

## ♻️ 4. **PUT** – Update an Existing Item

```python
@app.route("/api/books/<int:book_id>", methods=["PUT"])
def update_book(book_id):
    data = request.get_json()
    for book in books:
        if book["id"] == book_id:
            book["title"] = data.get("title", book["title"])
            book["author"] = data.get("author", book["author"])
            return jsonify(book)
    return jsonify({"error": "Book not found"}), 404
```

🧪 Example in Postman:
**PUT** → `http://127.0.0.1:5000/api/books/1`
**Body**:

```json
{
  "title": "The Alchemist (Updated)"
}
```

---

## ❌ 5. **DELETE** – Remove an Item

```python
@app.route("/api/books/<int:book_id>", methods=["DELETE"])
def delete_book(book_id):
    for i, book in enumerate(books):
        if book["id"] == book_id:
            removed = books.pop(i)
            return jsonify({"message": "Book deleted", "book": removed})
    return jsonify({"error": "Book not found"}), 404
```

🧪 Example:
**DELETE** → `http://127.0.0.1:5000/api/books/2`

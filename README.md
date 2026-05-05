# 📚 Book Inventory Management System

Full-stack CRUD app using Node.js · Express · MongoDB

## Folder Structure

```
book-app/
├── models/
│   └── Book.js          ← Mongoose schema
├── routes/
│   └── books.js         ← All 5 API endpoints
├── public/
│   └── index.html       ← Frontend (HTML + JS)
├── server.js            ← Express server + MongoDB connection
├── package.json
└── README.md
```

## Setup & Run

### 1. Install dependencies
```bash
cd book-app
npm install
```

### 2. Make sure MongoDB is running
- **Local:** `mongod` (MongoDB must be installed)
- **Atlas:** Set your connection string in MONGO_URI env variable

```bash
# Optional: use MongoDB Atlas
export MONGO_URI="mongodb+srv://<user>:<pass>@cluster.mongodb.net/bookdb"
```

### 3. Start the server
```bash
node server.js
```

Server runs at: **http://localhost:3000**

---

## API Endpoints

| Method | Route             | Action           |
|--------|-------------------|------------------|
| GET    | /api/books        | Fetch all books  |
| POST   | /api/books        | Add a new book   |
| GET    | /api/books/:id    | Get one book     |
| PUT    | /api/books/:id    | Update book      |
| DELETE | /api/books/:id    | Delete a book    |

### Example POST body (JSON)
```json
{
  "title": "The Alchemist",
  "isbn": "978-0061122415",
  "author": "Paulo Coelho",
  "genre": "Fiction",
  "price": 299,
  "stock": 10,
  "publishedYear": 1988
}
```

---

## Features
- ✅ List all books in a table
- ✅ Add new book via form
- ✅ Delete book with confirmation
- ✅ **Bonus:** Inline edit Price & Stock (click on any price/stock value)

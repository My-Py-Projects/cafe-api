# CafeAPI - RESTful Coffee Shop Management

## 🎯 Project Description  
CafeAPI is a lightweight and scalable RESTful API built with Flask and SQLAlchemy to manage coffee shop data. It provides complete CRUD functionality, including secure deletion, real-time price updates, and location-based search.

## 📦 Deliverables  
- Flask web application  
- SQLite database integration  
- SQLAlchemy ORM models  
- JSON-based API responses  
- Built-in HTML landing page  

## 🚀 Key Features  
- ☕ Retrieve a random café  
- 📍 Search cafés by location  
- 🧾 Add new cafés via form or API  
- 💸 Update coffee prices  
- 🔒 Secure café removal using API key

## 🛠️ Technologies Used  
| Component              | Technology            |
|------------------------|-----------------------|
| **Framework**          | Flask                 |
| **ORM**                | SQLAlchemy 2.0        |
| **Database**           | SQLite                |
| **Serialization**      | JSON                  |
| **Language**           | Python 3.10+          |

---

## ⚙️ API Endpoints

| Endpoint               | Method   | Description                      |
|------------------------|----------|----------------------------------|
| `/`                    | GET      | HTML interface / health check    |
| `/random`              | GET      | Get a random cafe                |
| `/all`                 | GET      | Retrieve all cafes               |
| `/search?location=...` | GET      | Search cafés by location         |
| `/add`                 | POST     | Add a new cafe (form-urlencoded) |
| `/update-price/<id>`   | PATCH    | Update the price of a cafe       |
| `/report-closed/<id>`  | DELETE   | Delete a cafe (requires API key) |

---

## ⚙️ Installation & Setup  

### 1. Clone the Repository  
```bash
git clone https://github.com/My-Py-Projects/cafe-api.git
cd cafe-api
```

### 2. Create Virtual Environment (Optional but recommended)  
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```

### 3. Install Dependencies  
```bash
pip install -r requirements.txt
```

> If `requirements.txt` doesn't exist yet:
```bash
pip install flask flask-sqlalchemy
pip freeze > requirements.txt
```

### 4. Run the Application  
```bash
python main.py
```

The server will be available at `http://127.0.0.1:8080`.

---

📚 **Full API Documentation:**  
[API documentation](https://documenter.getpostman.com/view/39954806/2sB2cYbL1i)

---

## 📌 Notes & Recommendations  
```plaintext
1. Security:
   - DELETE endpoint protected by a static API key (for demo purposes only)

2. Database:
   - SQLite is file-based and great for prototyping

3. Errors:
   - Consistent JSON error messages
   - Returns proper HTTP status codes (400, 403, 404)
```


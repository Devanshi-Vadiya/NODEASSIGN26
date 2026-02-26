# 🛒 Products REST API (Node.js + Express)

A simple RESTful API built using **Node.js** and **Express.js** to manage a collection of products.
The API supports fetching, creating, updating, and filtering products.

---

## 🔗 Project Links

**GitHub Repository:**
YOUR_GITHUB_LINK

**Live API (Render Deployment):**
YOUR_RENDER_LINK

**Postman Documentation:**
YOUR_POSTMAN_LINK

---

## 🚀 Steps to Run Locally

### 1️⃣ Clone the repository

```
git clone YOUR_GITHUB_LINK
```

### 2️⃣ Go inside the folder

```
cd products-api
```

### 3️⃣ Install dependencies

```
npm install
```

### 4️⃣ Start the server

```
node index.js
```

Server will start at:

```
http://localhost:3000
```

---

## 📌 Base URL

### Local

```
http://localhost:3000
```

### Deployed (Render)

```
YOUR_RENDER_LINK
```

---

## 📂 Product Object Structure

```
{
  "id": 1,
  "name": "Wireless Mouse",
  "category": "Electronics",
  "price": 799,
  "stock": 25,
  "rating": 4.3
}
```

---

## 📡 API Routes

| Method | Endpoint                         | Description              | Status Code |
| ------ | -------------------------------- | ------------------------ | ----------- |
| GET    | /                                | Check server             | 200         |
| GET    | /products                        | Get all products         | 200         |
| GET    | /products/:id                    | Get product by ID        | 200 / 404   |
| GET    | /products/category/:categoryName | Get products by category | 200 / 404   |
| POST   | /products                        | Create a new product     | 201         |
| PUT    | /products/:id                    | Replace full product     | 200 / 404   |
| PUT    | /products/:id/stock              | Update stock             | 200 / 404   |
| PUT    | /products/:id/price              | Update price             | 200 / 404   |

---

## 🧪 Sample Request & Response

### Create Product

**POST** `/products`

Request Body:

```
{
  "name": "Bluetooth Speaker",
  "category": "Electronics",
  "price": 1499,
  "stock": 18,
  "rating": 4.7
}
```

Response:

```
{
  "message": "Product created",
  "product": {
    "id": 6,
    "name": "Bluetooth Speaker",
    "category": "Electronics",
    "price": 1499,
    "stock": 18,
    "rating": 4.7
  }
}
```

---

### Get Product by ID

**GET** `/products/1`

Response:

```
{
  "id": 1,
  "name": "Wireless Mouse",
  "category": "Electronics",
  "price": 799,
  "stock": 25,
  "rating": 4.3
}
```

---

## 📊 Status Codes Used

| Code | Meaning               |
| ---- | --------------------- |
| 200  | Success               |
| 201  | Resource Created      |
| 404  | Product Not Found     |
| 500  | Internal Server Error |

---

## 🛠 Technologies Used

* Node.js
* Express.js
* Postman (API testing)
* Render (deployment)
* GitHub (version control)

---

## 👨‍💻 Author

**Your Name**

---

## 📜 Notes

* This API does not use a database (data stored in memory array)
* Restarting server resets products
* All routes are publicly accessible

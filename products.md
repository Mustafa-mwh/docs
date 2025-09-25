# 📦 Module Documentation – Products

## 1. Overview

This document provides technical details for the **Products Module** in the project. It includes implemented features, APIs, database schema, challenges, and notes to ensure consistency across the development team.

---

## 2. Features Implemented

- [x] Create new product
- [x] Edit product details (name, price, stock)
- [x] Delete product
- [ ] Product search & filtering (in progress)

---

## 3. API Endpoints

### 3.1 Create Product

```http
POST /api/v1/products
```

**Request Body**

```json
{
  "name": "iPhone 16",
  "price": 1200,
  "stock": 15,
  "category_id": 2
}
```

**Response**

```json
{
  "success": true,
  "message": "Product created successfully",
  "data": {
    "id": 101,
    "name": "iPhone 16",
    "price": 1200,
    "stock": 15
  }
}
```

---

### 3.2 Get All Products

```http
GET /api/v1/products
```

**Response Example**

```json
{
  "success": true,
  "data": [
    {
      "id": 101,
      "name": "iPhone 16",
      "price": 1200,
      "stock": 15
    },
    {
      "id": 102,
      "name": "Galaxy S25",
      "price": 1100,
      "stock": 25
    }
  ]
}
```

---

## 4. Database Schema

**Table: products**

| Column      | Type      | Constraints                 | Description       |
| ----------- | --------- | --------------------------- | ----------------- |
| id          | INT (PK)  | AUTO_INCREMENT              | Unique identifier |
| name        | VARCHAR   | NOT NULL                    | Product name      |
| price       | DECIMAL   | NOT NULL                    | Product price     |
| stock       | INT       | DEFAULT 0                   | Available stock   |
| category_id | INT (FK)  | REFERENCES categories(id)   | Product category  |
| created_at  | TIMESTAMP | DEFAULT CURRENT_TIMESTAMP   | Creation date     |
| updated_at  | TIMESTAMP | ON UPDATE CURRENT_TIMESTAMP | Last update date  |

---

## 5. Challenges & Notes

- Implemented stock validation to prevent negative values.
- Future improvement: Add image upload for products.
- Need to align search filters with frontend team.

---

## 6. Developer Info

- **Developer**: John Doe
- **Date Started**: 2025-09-20
- **Last Updated**: 2025-09-25

---

## ✅ Checklist

- [x] API tested with Postman
- [x] Database migration added
- [x] Unit tests created
- [ ] Integration tests pending

---

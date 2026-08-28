# 🛒 Olist E-Commerce Sales & Customer Analytics

## 📌 Project Overview

This project analyzes the **Olist Brazilian E-Commerce Public Dataset** using **MySQL** to understand customer behavior, sales performance, product and seller performance, delivery efficiency, and customer satisfaction.

The main goal of this project is to answer **real-world business questions using SQL** and convert transactional data into meaningful business insights.

---

## 🎯 Business Objectives

The project focuses on answering important business questions such as:

- 👥 How do customers behave across different states?
- 🔁 How many customers make repeat purchases?
- 💰 Which customers generate the highest revenue?
- 📈 Which product categories generate the most revenue?
- 🏆 Which products and sellers perform best?
- 🚚 How efficient is the delivery process?
- ⚠️ Which states and sellers have higher delivery delays?
- ⭐ Does delivery performance affect customer satisfaction?
- 📊 How does sales performance change month over month?
- 💎 Which customers can be classified as high-value customers?

---

## 🗄️ Dataset

The project uses the **Olist Brazilian E-Commerce Public Dataset**.

The dataset contains multiple related tables representing different parts of an e-commerce business.

### Main Tables

| Table | Purpose |
|---|---|
| `customers` | Customer information and location |
| `orders` | Order details and timestamps |
| `order_items` | Products included in each order |
| `products` | Product information and categories |
| `sellers` | Seller information and location |
| `payments` | Payment details and transaction values |
| `reviews` | Customer review and rating information |

---

## 🔗 Database Relationships

The main relationships used in the analysis are:

```text
customers
    │
    │ customer_id
    ↓
orders
    │
    ├──────────────→ payments
    │
    ├──────────────→ reviews
    │
    ↓
order_items
    │
    ├──────────────→ products
    │
    └──────────────→ sellers

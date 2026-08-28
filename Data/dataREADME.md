# 🗄️ Dataset

This project uses the **Brazilian E-Commerce Public Dataset by Olist**, obtained from Kaggle.

The dataset contains approximately 100,000 e-commerce orders from 2016 to 2018 and is divided into multiple relational CSV files. These files cover customers, orders, products, sellers, payments, reviews, and geolocation data.

## 📌 Dataset Source

**Platform:** Kaggle

**Dataset:** Brazilian E-Commerce Public Dataset by Olist

🔗 https://www.kaggle.com/olistbr/brazilian-ecommerce

The original dataset is not included in this repository to keep the project lightweight.

---

## 📊 Dataset Composition

| Dataset | Rows | Columns | Description |
|---|---:|---:|---|
| `olist_customers_dataset.csv` | 99,441 | 5 | Customer information and location |
| `olist_orders_dataset.csv` | 99,441 | 8 | Order status, purchase and delivery timestamps |
| `olist_order_items_dataset.csv` | 112,650 | 7 | Products, sellers, prices and freight for each order item |
| `olist_order_payments_dataset.csv` | 103,886 | 5 | Payment methods, installments and payment values |
| `olist_order_reviews_dataset.csv` | 99,224 | 7 | Customer review scores and review information |
| `olist_products_dataset.csv` | 32,951 | 9 | Product information and category details |
| `olist_sellers_dataset.csv` | 3,095 | 4 | Seller information and location |
| `olist_geolocation_dataset.csv` | 1,000,163 | 5 | Brazilian ZIP-code geographic information |
| `product_category_name_translation.csv` | 71 | 2 | Portuguese-to-English product category mapping |

---

## 🔗 Tables Used in This Project

The SQL analysis primarily uses these tables:

- `customers`
- `orders`
- `order_items`
- `products`
- `sellers`
- `payments`
- `reviews`

The geolocation and category-translation datasets are part of the original Kaggle dataset but were not required for the main SQL analysis.

## 🔄 Main Relationships

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

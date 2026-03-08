# 🧠 Cognicare: Mental Health Marketplace — Database Design & Business Intelligence

![SQL](https://img.shields.io/badge/Language-SQL-4479A1?style=flat-square&logo=mysql)
![Python](https://img.shields.io/badge/Analysis-Python-3776AB?style=flat-square&logo=python)
![DB](https://img.shields.io/badge/Database-MariaDB%20%2F%20MySQL-00758F?style=flat-square)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)

## Overview

Cognicare is a conceptual **mental health marketplace** connecting users with therapists, wellness coaches, and yoga instructors — while also offering a product store for mental health-related items. Developed in collaboration with a peer, this project covers the full lifecycle of database development: designing the entity-relationship model, building the relational schema in MySQL, populating it with realistic dummy data, and running managerial queries to extract actionable business insights.

> **Business context:** Cognicare operates as a two-sided marketplace — users book appointments with service providers and purchase wellness products from suppliers. The database supports operations across appointments, orders, payments, reviews, and provider management.

---

## Project Scope

| Phase | Description |
|-------|-------------|
| **Conceptual Design** | Entity-Relationship (ER) diagram covering all entities and relationships |
| **Logical Design** | Relational schema normalised across 13 tables |
| **Physical Implementation** | Database built and populated in MariaDB via phpMyAdmin |
| **Business Intelligence** | Managerial SQL queries and Python visualisations for insights |

---

## Database Schema

The database consists of **13 interrelated tables:**

| Table | Description |
|-------|-------------|
| `user` | Registered marketplace users |
| `service_provider` | Therapists, coaches, and yoga instructors |
| `service` | Services offered (therapy, yoga, meditation, coaching) |
| `appointment` | Bookings linking users, providers, and services |
| `product` | Wellness products available for purchase |
| `category` | Product and service categories (Therapy, Yoga, Mindfulness, etc.) |
| `order` | Customer product orders |
| `order_detail` | Line items within each order |
| `payment` | Payment records for both orders and appointments |
| `supplier` | Product suppliers with lead time and contact info |
| `supplier_product` | Many-to-many: which suppliers provide which products |
| `product_rating` | User ratings and reviews for products |
| `service_review` | User reviews for completed appointments |

---

## Business Insights & Queries

The analysis answers key managerial questions including:

- **Product performance:** Distribution of product ratings; top 10 most ordered products
- **Category demand:** Order volume by product/service category
- **Appointment analytics:** Appointment status breakdown (Completed / Cancelled / Scheduled) by provider and service type
- **Revenue analysis:** Total appointment value by service category and provider
- **Supplier performance:** Delivery lead times and product availability by supplier

---

## Visualisations Produced

- **Rating Distribution** — Count plot of product ratings across the catalogue
- **Order Count by Category** — Bar chart of demand across product/service categories
- **Top 10 Most Ordered Products** — Horizontal bar chart ranked by order volume

---

## Repository Structure

```
├── cognicare.sql                  # Full database dump (schema + data, MariaDB)
├── cognicare.ipynb                # Python notebook: queries, analysis, visualisations
├── ER_diagram.pdf                 # Entity-relationship conceptual model
└── README.md
```

> **Note:** CSV data exports are not included. The full dataset is available via the `.sql` dump file, which can be imported into any MySQL/MariaDB instance.

---

## How to Run

### Option A — Import the database (MySQL/MariaDB)
1. Install [XAMPP](https://www.apachefriends.org/) or any MySQL environment
2. Open phpMyAdmin and create a new database named `cognicare`
3. Import `cognicare.sql` via the Import tab
4. Run queries directly in phpMyAdmin or any SQL client

### Option B — Explore the analysis notebook
1. Open `cognicare.ipynb` in **Google Colab** or Jupyter
2. Export tables from your imported database as CSVs and upload when prompted
3. Run all cells to reproduce the visualisations

**Required Python packages:**
```
pandas, matplotlib, seaborn
```
---

## Author

**Shafaq Karim** — Graduate student in Business Analytics, Ivey Business School
[LinkedIn](https://www.linkedin.com/in/shafaqkarim/) · [Portfolio](https://shafaq-karim-t07p6o9.gamma.site/)

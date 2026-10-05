# MongoDB E-Commerce Database Project

A NoSQL document database built for an e-commerce system, demonstrating hybrid 
data modeling, schema validation, and full CRUD operations.

## What This Project Shows

- Hybrid data modeling: embedded order items, referenced customers and products
- Schema validation rules
- Full CRUD operations including nested array queries
- Query operators: `$gt`, `$in`, `$regex`, projections

## Tools

MongoDB • mongosh • MongoDB Compass

## Data Model

**Embedded** — `orders.items[]` stores price and quantity at purchase time, 
preserving historical transaction data.

**Referenced** — Customers and products are referenced by ID (`customer_id`, 
`product_id`) to avoid duplication.

**Relationships**
- `orders.customer_id` → `customers._id`
- `orders.items[].product_id` → `products._id`

## Queries Demonstrated

| Operation | Description |
|---|---|
| Create | Insert a customer and a linked order |
| Read | Filter by price (`$gt`) and category (`$in`) |
| Read | Regex search on email (`$regex`) |
| Read | Filter on nested `items.product_id` |
| Update | `$set` order status and customer city |
| Delete | Remove test records |

## Files

- `mongodb-ecommerce-project.pdf` — full report with screenshots
- `mongodb-ecommerce-project.txt` — all queries in order

## How to Run

1. `use ecommerce_portfolio`
2. Import `customers.json`, `products.json`, `orders.json`
3. Run queries from the `.txt` file in order

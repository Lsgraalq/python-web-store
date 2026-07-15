# python-web-store

> **Created: March 2024** — Django e-commerce project.

A working **online store** built with **Django** — the most complete backend project of this period. It covers the core of an e-commerce flow: a product catalog, a session-based shopping cart, and order placement.

## Features

### Shop
- **Categories** and **Products** with slugs, images, descriptions, prices, and availability flags.
- Product **list** (all products or filtered by category) and product **detail** pages.
- Database indexes on key fields and SEO-friendly URLs via `get_absolute_url` / slugs.

### Cart
- A **session-based cart** (`cart/cart.py`) supporting add / update quantity / remove / clear.
- Iterable cart that resolves products, computes per-item and total prices with `Decimal`.
- Exposed to templates through a **context processor**.

### Orders
- **Order** and **OrderItem** models with customer details and a `paid` flag.
- Order creation form and confirmation flow; total cost computed from order items.

## Structure

| App       | Responsibility |
|-----------|----------------|
| `shop`    | Catalog: categories, products, list/detail views. |
| `cart`    | Session cart logic, forms, context processor. |
| `orders`  | Order + order item models, order creation. |
| `core`    | Project configuration. |

## Running

```bash
pip install django pillow
python manage.py migrate
python manage.py runserver
```

## Stack

- Python 3
- Django
- Pillow (product images)
- SQLite

## License

MIT © 2024 Lsgraalq — see [LICENSE](LICENSE).

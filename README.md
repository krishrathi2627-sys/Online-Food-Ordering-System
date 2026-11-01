# Online-Food-Ordering-System
Online Food Ordering System - Software Engineering
# 🍽️ Online Food Ordering System

[![CI](https://github.com/YOUR-USERNAME/online-food-ordering-system/actions/workflows/ci.yml/badge.svg)](https://github.com/YOUR-USERNAME/online-food-ordering-system/actions)

A full-stack web application where customers browse a menu, order food online and track orders, and restaurant staff manage the menu and order lifecycle. Built as a **Software Engineering** course project with complete documentation (SRS, design diagrams, test plan).

**Tech stack:** Python 3 · Flask · SQLite · Jinja2 · HTML/CSS · pytest · GitHub Actions

## Features
**Customer**
- Register / login (hashed passwords)
- Browse, search and filter the menu
- Cart with quantity updates
- Checkout with delivery address and (simulated) payment method
- Order history, order details, cancel while order is "Placed"

**Admin**
- Dashboard: orders, revenue, customers, menu items
- Menu management: add, edit, delete, enable/disable items
- Order management: filter by status and update through the lifecycle

**Security:** CSRF tokens, parameterised SQL, role-based access, open-redirect protection.

## Quick start

```bash
git clone https://github.com/YOUR-USERNAME/online-food-ordering-system.git
cd online-food-ordering-system

python -m venv .venv
# Windows: .venv\Scripts\activate      macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt

python app.py
```

Open <http://127.0.0.1:5000>. The database (`food.db`) and sample menu are created automatically on first run.

**Default admin login:** `admin@food.com` / `Admin@123`
Change it before any real deployment, for example `ADMIN_PASSWORD=MyStrongPass python app.py` on a fresh database. Also set `SECRET_KEY` to a long random value.

## Run the tests
```bash
python -m pytest -v
```

## Project structure
```
online-food-ordering-system/
├── app.py                 # Flask app factory, routes, business logic
├── schema.sql             # Database schema
├── requirements.txt
├── templates/             # Jinja2 views (customer + admin)
├── static/style.css
├── tests/test_app.py      # 16 automated tests
├── docs/
│   ├── SRS.md             # Software Requirements Specification
│   ├── DESIGN.md          # Architecture, UML/ER diagrams (Mermaid)
│   └── TEST_PLAN.md       # Test cases and traceability
└── .github/workflows/ci.yml
```

## Documentation
- [Software Requirements Specification](docs/SRS.md)
- [System Design (architecture, ER, sequence, state diagrams)](docs/DESIGN.md)
- [Test Plan](docs/TEST_PLAN.md)

## Future enhancements
Real payment gateway, email/SMS notifications, ratings and reviews, delivery tracking, multi-restaurant support, REST API + mobile app.

## License
MIT. See [LICENSE](LICENSE).

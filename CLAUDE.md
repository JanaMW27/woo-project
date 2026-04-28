# CLAUDE.md — WooCommerce Store Health Widget

This file provides context for Claude (and team members) working on the `woo-project` repository. Read this before making any contributions or asking Claude for help.

---

## 📌 Project Overview

**Project name:** WooCommerce Store Health Widget  
**Goal:** Build a WooCommerce widget for WooCore that displays store health metrics and provides actionable recommendations to improve a store's visibility, performance, conversion rate, and profit.

---

## 👥 Team

- **Size:** 2–3 people
- **Background:** Designers — not developers. We rely on Claude to write and explain all code.
- **Working style:** We describe what we want in plain language and Claude implements it.

> ⚠️ Please write all code with clear inline comments. Assume the reader is not a developer.

---

## 🛠️ Tech Stack

| Layer | Technology | Why |
|---|---|---|
| Backend | **PHP** | Required for WordPress/WooCommerce plugins |
| Frontend | **Vanilla JS + HTML/CSS** | Simple, no build tools needed |
| Styling | **CSS with WordPress conventions** | Fits naturally into WP admin |
| Standards | **WordPress Coding Standards (WPCS)** | Standard for all WP/WooCommerce plugins |

> No React or Vue — keep it simple and maintainable by non-developers.

---

## 🏗️ Architecture

This is a **WooCommerce plugin** that registers a widget in the WordPress admin dashboard. It:

1. Reads store data via WooCommerce REST API / WP hooks
2. Scores store health across 4 dimensions: **Visibility**, **Performance**, **Conversion**, **Profit**
3. Displays scores and improvement suggestions in WP Admin

### Folder structure (planned)
woo-project/
├── woo-health-widget.php
├── includes/
│   ├── class-health-checker.php
│   └── class-widget.php
├── assets/
│   ├── css/widget.css
│   └── js/widget.js
├── templates/
│   └── widget-dashboard.php
├── .gitignore
└── README.md

---

## 🐳 Local Development

The team uses **Docker**. Mount the plugin as a volume:

```yaml
volumes:
  - ./woo-project:/var/www/html/wp-content/plugins/woo-health-widget
```

Activate via **WP Admin → Plugins**.

---

## 🧭 Widget Feature Scope

### 1. 🔍 Visibility
SEO checks — product titles, meta descriptions, sitemaps

### 2. ⚡ Performance
Page speed, image optimization status

### 3. 🛒 Conversion
Missing product images/descriptions, checkout experience

### 4. 💰 Profit
Best/worst products, upsell opportunities, abandoned cart

---

## ✅ Coding Guidelines

1. **Comment everything** in plain English
2. **Keep files small** — one responsibility per file
3. Follow **[WordPress Coding Standards](https://developer.wordpress.org/coding-standards/)**
4. Use **WordPress/WooCommerce built-in functions** wherever possible
5. **No external dependencies** unless absolutely necessary
6. All user-facing strings must use `__()` or `_e()` for translations

---

## 🔗 Useful Resources

- [WooCommerce Developer Docs](https://developer.woocommerce.com/)
- [WordPress Plugin Handbook](https://developer.wordpress.org/plugins/)
- [WooCommerce REST API](https://woocommerce.github.io/woocommerce-rest-api-docs/)

---

## 🗂️ Repository

- **GitHub:** https://github.com/JanaMW27/woo-project
- **Branches:** Work on feature branches, merge to `main` when ready
- **Commits:** Use plain English, e.g. `Add health score for visibility section`

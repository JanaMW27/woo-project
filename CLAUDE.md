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

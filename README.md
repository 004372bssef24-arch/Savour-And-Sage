<div align="center">

# 🍽️ Savour & Sage

**Modern Full-Stack Restaurant Operations, Reservation & Loyalty Management Platform**

[![Node Version](https://img.shields.io/badge/Node.js-18%2B-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![Frontend](https://img.shields.io/badge/Frontend-HTML5%20%2F%20CSS3%20%2F%20ES6%2B-E34F26?style=for-the-badge&logo=javascript&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Backend](https://img.shields.io/badge/Backend-Express.js-000000?style=for-the-badge&logo=express&logoColor=white)](https://expressjs.com/)
[![Database](https://img.shields.io/badge/Database-PostgreSQL%20%2F%20Sequelize-336791?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![License](https://img.shields.io/badge/License-MIT-gold?style=for-the-badge)](LICENSE)

<p align="center">
  <a href="#overview">Overview</a> •
  <a href="#system-architecture">Architecture</a> •
  <a href="#core-modules">Core Modules</a> •
  <a href="#tech-stack">Tech Stack</a> •
  <a href="#installation--setup">Quickstart</a> •
  <a href="#environment-configuration">Configuration</a> •
  <a href="#license">License</a>
</p>

---

</div>

## 📌 Overview

**Savour & Sage** is a full-stack web application engineered for modern hospitality management. It bridges customer-facing dining interactions (real-time table booking, interactive dynamic menus, loyalty rewards tracking, and operating schedule inquiries) with a secure back-office administrative portal for staff management and operational oversight.

Designed with modular frontend components, asynchronous REST APIs, and structured relational persistence, Savour & Sage streamlines restaurant table turnover and simplifies dining workflow management.

---

## 🏛️ System Architecture

```text
Savour-and-Sage/
├── 📁 admin/                 # Back-office administration portal & dashboard
├── 📁 backend/               # Express.js REST API, controllers, and ORM models
│   ├── config/               # Database connection and environment config
│   ├── controllers/          # Business logic handlers (Reservations, Menu, Loyalty)
│   ├── models/               # Relational data schemas & ORM entities
│   └── routes/               # API route definitions & middleware
│
├── 📁 frontend/              # Client-side scripts, assets, and views
├── 📄 business-hours.html    # Dynamic operating schedule & holiday calendar
├── 📄 login.html             # Customer authentication & staff portal entry
├── 📄 loyalty.html           # Rewards point engine & tier progress tracker
├── 📄 menu.html              # Filterable digital catalog with price breakdowns
├── 📄 reservations.html      # Real-time table booking & guest party configuration
├── 🎨 main.css               # Global responsive design tokens & styling
└── ⚙️ package.json           # Node.js dependencies and script definitions

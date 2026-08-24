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
```

## ⚡ Core Modules

📅 Smart Reservation Engine: Dynamic table allocation system enabling guests to schedule dining slots, specify party sizes, request dietary accommodations, and receive real-time booking confirmation.

📜 Interactive Digital Menu: Categorized food and beverage catalog featuring real-time price updates, ingredient transparency, and allergen indicators.

💎 Customer Loyalty System: Automated point-accumulation engine tracking customer visit frequency, milestone tiers, and redemption credits.

🕒 Operating Hours & Schedule Manager: Real-time business status indicators displaying open/closed states, operational shifts, and special holiday timings.

🛡️ Staff & Admin Control Center: Isolated back-office dashboard providing staff members with real-time floor monitoring, reservation updates, and catalog manipulation.

## 🛠️ Tech Stack

Frontend: Semantic HTML5, Modular CSS3 (Custom Design System), Vanilla ES6+ JavaScript

Backend Runtime: Node.js, Express.js

Data Access & ORM: Sequelize ORM

Database Engine: PostgreSQL (or SQLite/MySQL compatible)

Authentication & Security: Bcrypt hashing, secure session management, CORS protection

Tooling & Environment: Dotenv, NPM package ecosystem

## 🚀 Installation & Setup

Prerequisites
Node.js (v18.0.0 or higher)

PostgreSQL (or local database instance)

1. Clone the Repository
Bash
git clone [https://github.com/004372bssef24-arch/savour-and-sage.git](https://github.com/004372bssef24-arch/savour-and-sage.git)
cd savour-and-sage
2. Install Dependencies
Bash
npm install
3. Environment Configuration
Create a .env file in the root directory:

Code snippet
PORT=5000
NODE_ENV=development
DB_HOST=localhost
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_NAME=savour_and_sage_db
DB_PORT=5432
SESSION_SECRET=your_jwt_or_session_secret
4. Database Migration & Initialization
Bash
#Initialize schema and seed default menu items
npm run db:migrate
5. Launch the Server
Bash
#Start backend server
npm run dev

#Or standard production start
npm start
Access the client application in your browser at http://localhost:5000.

## 📄 License
This project is licensed under the MIT License — see the LICENSE file for details.

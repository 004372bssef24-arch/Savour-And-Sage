# PROJECT_STATE.md

## Section 1: Project Overview
- **Project Name:** Savour & Sage
- **Description:** Farm-to-table restaurant management system.
- **Tech Stack:** Node.js, Express, PostgreSQL, Sequelize ORM, Vite, Vanilla JavaScript.
- **Repository Structure:**
  - `/backend`: Node.js/Express REST API
  - `/frontend`: Static site with dynamic JS functionality
  - `/admin`: Admin dashboard area

## Section 2: Backend Status
- **Models:**
  - `User`: id, name, email, password_hash, loyalty_points, tier, etc.
  - `MenuItem`: id, category, name, price, description, etc.
  - `Reservation`: id, user_id, date, guests, status, etc.
  - `LoyaltyPoints`: id, user_id, points, type, etc.
- **Routes:**
  - `/api/auth`: Register, login, logout, etc.
  - `/api/menu`: CRUD for menu items.
  - `/api/reservations`: CRUD for reservations.
  - `/api/admin`: Dashboard metrics.
- **Controllers:** Implemented basic CRUD for all entities.
- **Env:** `.env` file required for configuration.

## Section 3: Frontend Status
- **Pages:** Home, Menu, Reservation Form, User Dashboard.
- **Components:** Navigation, Login Modal, Menu Tabs, Activity/Reservations dashboard lists.
- **API Status:** Integrated; `populateMenu()` dynamically fetches from `GET /api/menu`.
- **Styling:** CSS provided via `style.css`.

## Section 4: Known Issues (CRITICAL)
- **IntersectionObserver:** Not triggering correctly on hash navigation to reveal sections.
- **CSS Paths:** Potential resolution issues with some assets/imports.
- **Auth Flow:** Currently using JWT + localStorage; needs conversion to `HttpOnly` cookies.
- **Validation:** Server-side `express-validator` implemented, but frontend forms lack detailed client-side error feedback.
- **State Management:** Dashboard stats and reservation lists need more robust UI updates.

## Section 5: Next Steps (Prioritized)
### Priority 1 (Blocking):
- Fix CSS/asset resolution.
- Fix section visibility/IntersectionObserver.
- Add error boundaries to frontend API calls.

### Priority 2 (Core Features):
- Refactor Auth to use `HttpOnly` cookies.
- Complete reservation booking form submission logic.
- Complete full dashboard interactions (reservation history).

### Priority 3 (Polish):
- Implement loading spinners/states for all async actions.
- Add proper toast notifications for success/error feedback.
- Finalize responsive design adjustments.

## Section 6: Architecture Decisions
- **Vite:** Chosen for modern, fast build setup and built-in proxying capabilities for backend development.
- **Sequelize:** Provides a structured, ORM-based approach to interacting with the PostgreSQL database.
- **Vanilla JS:** Minimalist approach to keep the project lightweight and avoid dependency bloat.
- **Auth:** Initial setup uses standard JWT, moving towards `HttpOnly` cookies for increased security.

## Section 7: Database Schema
- **Tables:** `users`, `menu_items`, `reservations`, `loyalty_transactions`, `activity_logs`.
- **Relationships:** Reservations are linked to Users via `user_id`.
- **Migration Status:** Managed via local `schema.sql` and `Sequelize.sync()`.

## Section 8: API Endpoints
| Method | Path | Description | Auth Required | Status |
| :--- | :--- | :--- | :--- | :--- |
| POST | /api/auth/register | Register a new user | No | Working |
| POST | /api/auth/login | Login and get JWT | No | Working |
| GET | /api/menu | Get menu items | No | Working |
| POST | /api/reservations | Create reservation | Yes | Working |

## Section 9: Environment Variables
- `PORT`
- `DATABASE_URL`
- `JWT_SECRET`
- `JWT_REFRESH_SECRET`
- `EMAIL_USER`
- `EMAIL_PASS`
- `CLIENT_URL`

## Section 10: Testing Instructions
- **Backend:** Run `npm start` in the `backend/` directory.
- **Frontend:** Run `npm run dev` in the root (assuming Vite is used).
- **Seeding:** Run `node seed.js` in the `backend/` folder to populate the database.

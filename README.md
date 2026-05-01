# HisabKitab
### Overview

**HisabKitab** (Hindi: *हिसाब-किताब* — "accounts and records") digitizes the traditional paper based khata system used widely in India. Users can manage transactions with multiple parties, track outstanding dues, and maintain a clear record of who owes whom.

---

### Tech Stack

| Layer      | Technology                                              |
|------------|---------------------------------------------------------|
| Frontend   | React 18 (Vite), Tailwind CSS, React Router v7, Day.js |
| Backend    | Node.js, Express.js                                     |
| Database   | MongoDB (Mongoose ODM)                                  |
| Auth       | JWT (JSON Web Tokens)                                   |
| Deployment | Vercel (frontend), custom domain                        |

---

### Project Structure

```
hisabkitab/
├── client/
│   └── src/
│       ├── components/       # AddCustomer, Transact, EditTransact
│       ├── contexts/         # UserContext (global auth state)
│       └── pages/            # Home, Login, Register, Dashboard,
│                             # CustomerView, SupplierView, Reports, Settings
│
└── server/
    └── src/
        ├── config/           # MongoDB connection
        ├── controllers/      # auth, customer, transaction logic
        ├── middleware/        # JWT auth
        ├── models/           # User, Customer, Transaction, Record
        └── routes/           # auth, customer, transaction routes
```

---

### Getting Started

#### Prerequisites

- Node.js v18+
- MongoDB (local or Atlas)

#### Environment Variables

Copy the example files and fill in your values:

```bash
cp server/.env.example server/.env
cp client/.env.example client/.env
```

Refer to `.env.example` in each directory for the required variables.

#### Installation

```bash
# Install backend dependencies
cd server
npm install

# Install frontend dependencies
cd ../client
npm install
```

### Running the Project

```bash
# Start the backend server
cd server
npm run start
# Runs at http://localhost:5000

# Start the frontend (in a separate terminal)
cd client
npm run dev
# Runs at http://localhost:5173
```

---

<!-- ## Screenshots -->
<!---->
<!-- | Landing | Dashboard | Transactions | -->
<!-- |---------|-----------|--------------| -->
<!-- | ![](./screenshots/screenshot-landing.png) | ![](./screenshots/screenshot-dashboard.png) | ![](./screenshots/screenshot-transaction.png) | -->
<!---->

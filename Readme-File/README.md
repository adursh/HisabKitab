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
├── IPR-Submission-Proof/
├── Report-and-PPT/
│   ├── HisabKitab_Report.docx
│   └── HisabKitab_Presentation.pptx
├── Readme-File/
│   └── README.md
└── Source-Code/
    ├── client/
    │   └── src/
    │       ├── components/       # AddCustomer, Transact, EditTransact
    │       ├── contexts/         # UserContext (global auth state)
    │       └── pages/            # Home, Login, Register, Dashboard,
    │                             # CustomerView, SupplierView, Reports, Settings
    └── server/
        └── src/
            ├── config/           # MongoDB connection
            ├── controllers/      # auth, customer, transaction logic
            ├── middleware/       # JWT auth
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
cd Source-Code
cp server/server.env.example server/.env
cp client/client.env.example client/.env
```

Refer to the example environment files in each directory for the required variables.

#### Installation

```bash
# Install backend dependencies
cd Source-Code
cd server
npm install

# Install frontend dependencies
cd ../client
npm install
```

### Running the Project

```bash
# Start the backend server
cd Source-Code/server
npm run start
# Runs at http://localhost:5000

# Start the frontend (in a separate terminal)
cd Source-Code/client
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

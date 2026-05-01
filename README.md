# 📒 HisabKitab — Digital Ledger Management App

> A modern, mobile-friendly digital khata (ledger) application inspired by OkCredit, enabling small business owners and individuals to track credit/debit transactions with their contacts seamlessly.

🌐 **Live Demo:** [hisabkitab.adursh.me](http://hisabkitab.adursh.me)

---

## 📌 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Environment Variables](#environment-variables)
- [Running the Project](#running-the-project)
- [Screenshots](#screenshots)
- [Author](#author)

---

## Overview

**HisabKitab** (Hindi: *हिसाब-किताब* — meaning "accounts and records") is a full-stack web application that digitizes the traditional paper-based khata (ledger) system used widely in India. It allows users to manage financial transactions with multiple parties, track outstanding dues, and maintain a clear record of who owes whom — all in one place.

This project was developed as part of the **Innovation and Opportunity in Higher Education (IOHE – 22CS422)** course at **Chitkara University Institute of Engineering & Technology**, BE-CSE, Batch 2022, Semester 8.

---

## Features

- 🔐 **User Authentication** — Secure JWT-based registration and login
- 👥 **Party Management** — Add and manage multiple contacts/parties
- 💰 **Transaction Tracking** — Log "Given" (debit) and "Received" (credit) entries per party
- 🧾 **Running Balance** — Auto-calculated net balance for each party
- 📱 **WhatsApp-style UI** — Transaction bubbles with color-coded debit (red) / credit (green) display
- 📊 **Dashboard Overview** — Summary of total outstanding dues across all parties
- 🔍 **Search** — Quickly find parties by name
- 📅 **Transaction History** — Date-wise chronological log per party

---

## Tech Stack

| Layer      | Technology                        |
|------------|-----------------------------------|
| Frontend   | React.js (Vite), CSS              |
| Backend    | Node.js, Express.js               |
| Database   | MongoDB (Mongoose ODM)            |
| Auth       | JWT (JSON Web Tokens), bcrypt     |
| Deployment | Custom domain — hisabkitab.adursh.me |

---

## Project Structure

```
hisabkitab/
├── client/                  # React + Vite frontend
│   ├── public/
│   └── src/
│       ├── components/      # Reusable UI components
│       ├── pages/           # Route-level pages (Login, Dashboard, Party)
│       ├── context/         # Auth context / global state
│       ├── api/             # Axios API call helpers
│       └── App.jsx
│
├── server/                  # Node.js + Express backend
│   ├── models/              # Mongoose schemas (User, Party, Transaction)
│   ├── routes/              # Express route handlers
│   ├── middleware/          # JWT auth middleware
│   ├── controllers/         # Business logic
│   └── server.js
│
├── .env.example             # Environment variable template
├── README.md
└── package.json
```

---

## Getting Started

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v18 or above)
- [MongoDB](https://www.mongodb.com/) (local or Atlas cloud instance)
- [Git](https://git-scm.com/)

### Clone the Repository

```bash
git clone https://github.com/<your-username>/hisabkitab.git
cd hisabkitab
```

---

## Environment Variables

Create a `.env` file in the `server/` directory based on `.env.example`:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
```

Create a `.env` file in the `client/` directory:

```env
VITE_API_BASE_URL=http://localhost:5000/api
```

---

## Running the Project

### 1. Install Dependencies

```bash
# Install backend dependencies
cd server
npm install

# Install frontend dependencies
cd ../client
npm install
```

### 2. Start the Backend Server

```bash
cd server
npm run dev
```

The backend will run at `http://localhost:5000`

### 3. Start the Frontend

```bash
cd client
npm run dev
```

The frontend will run at `http://localhost:5173`

---

## Screenshots

### 🏠 Landing Page
![Landing Page](screenshots/screenshot-landing.png)

### 🔐 Login
![Login Page](screenshots/screenshot-login.png)

### 📝 Registration (3-Step Flow)
![Register Page](screenshots/screenshot-register.png)

### 📊 Dashboard — Summary & Customer List
![Dashboard](screenshots/screenshot-dashboard.png)

### 💸 Party Ledger — Transaction Bubbles
![Transaction View](screenshots/screenshot-transaction.png)

### 📈 Reports & Summary
![Reports Page](screenshots/screenshot-reports.png)

---

## Author

**Adarsh**
BE – Computer Science & Engineering, Batch 2022
Chitkara University Institute of Engineering & Technology

---

## License

This project is the intellectual property of the author. Unauthorized copying, redistribution, or commercial use without explicit permission is prohibited.

© 2026 Adarsh. All rights reserved.
```

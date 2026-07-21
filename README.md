# Day 78: Connecting Login Gateway & Frontend Protected Routes

A full-stack MERN application built to bridge client-side authentication with server-side security. This module focuses on handling JWT tokens inside browser local storage, creating custom API instances using Axios, and enforcing client-side route protection.

---

## 🚀 Key Learning Objectives

- **Axios Centralization:** Configured a centralized Axios base instance (`apiInstance.js`) pointed at the backend gateway.
- **Client Auth Integration:** Managed asynchronous token acquisition upon user login and committed tokens to `localStorage`.
- **Protected Component Wrapper:** Implemented `<ProtectedRoutes />` to intercept unauthenticated layout access and redirect users to the login screen.
- **CORS Middleware Setup:** Enabled `cors` middleware on Express server to accept requests from frontend origins.

---

## 🛠️ Tech Stack

- **Frontend:** React 19, React Router v7, Axios, Tailwind CSS v4, Vite
- **Backend:** Node.js, Express.js v5, Mongoose v9, JsonWebToken, Bcryptjs

---

## 📁 Repository Architecture

```text
├── backend/
│   ├── config/          # MongoDB Atlas connection setup
│   ├── controllers/     # Task business logic
│   ├── middleware/      # JWT verification middleware
│   ├── models/          # Task & User Mongoose schemas
│   ├── routes/          # Express API route declarations
│   ├── security/        # Auth hashing & login token generator
│   └── main.js          # Express app instance with CORS enabled
└── frontend/
    ├── src/
    │   ├── api/         # Axios instance setup
    │   ├── components/  # ProtectedRoutes component wrapper
    │   └── pages/       # Login, Register, Home pages
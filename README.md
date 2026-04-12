# Deplomentment 

    https://blood-bank-tracking-system.netlify.app


# Blood Bank Tracking System



<p align="center">
  <strong>A full-stack platform for donor registration, blood availability discovery, and blood request coordination.</strong>
</p>

<p align="center">
  Built to simplify communication between donors, blood banks, managers, and administrators through a role-based workflow.
</p>

---

## Overview

The **Blood Bank Tracking System** is a full-stack web application that helps users search for available blood units, register as donors, authenticate into role-based dashboards, and coordinate urgent blood requests.

The system combines a **React + Vite frontend** with a **Node.js + Express backend**, backed by **MongoDB** for donor data storage. It also integrates with **UltraMsg/WhatsApp messaging** to notify donors during urgent blood requests.

---



### Architecture Summary
- **Frontend** serves the user interface for public users, donors, managers, and admins.
- **Backend API** handles authentication, donor registration, and blood request workflows.
- **MongoDB** stores user accounts, roles, blood groups, and donor metadata.
- **Static dataset layer** provides blood bank availability data through `bloodbanks.json`.
- **Messaging integration** sends request alerts through UltraMsg WhatsApp APIs.

---

## Core Features

- **Role-based user flows**
  Supports separate experiences for public users, donors, managers, and admins through dedicated dashboards and route-level separation.

- **Donor registration and authentication**
  Enables donor signup and login with hashed passwords using `bcryptjs` and persistent storage in MongoDB.

- **Blood group availability search**
  Allows users to filter blood banks by state, district, and blood group using the local blood bank dataset.

- **Urgent donor notification workflow**
  Matches donors by blood type and triggers WhatsApp message delivery for emergency blood requests.

- **Manager-facing blood request interface**
  Provides a dedicated dashboard for blood bank managers to review stock visibility and initiate request actions.

- **Admin dashboard foundation**
  Includes centralized views for blood bank summaries, transfer reporting, and future administrative workflows.

- **Client-side state management**
  Uses Zustand for lightweight authentication state handling across the frontend.

- **Modern frontend delivery**
  Built with Vite for fast local development, efficient bundling, and straightforward deployment to static hosting platforms.

---

## Tech Stack

### Frontend
- React 18
- Vite
- React Router
- Tailwind CSS
- Zustand
- Axios
- Lucide React
- React Hot Toast
- Chart.js / react-chartjs-2
- jsPDF

### Backend
- Node.js
- Express
- MongoDB
- Mongoose
- bcryptjs
- dotenv
- cors
- cookie-parser
- Twilio / UltraMsg-related integrations

### Deployment
- Render for backend hosting
- Netlify for frontend hosting

---
## How to run the project
## BACKEND:
cd backend
npm install
npm start
The backend will run on:   http://localhost:5000

## FRONTEND:
Open a new terminal:
cd frontend
npm install
npm run dev

## Repository Structure

```bash
Blood_Bank_Tracking_System/
├── backend/
│   ├── models/
│   │   └── userModel.js
│   ├── .env
│   ├── package.json
│   └── server.js
├── frontend/
│   ├── public/
│   │   └── bloodbanks.json
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── store/
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── .env
│   └── package.json
└── README.md

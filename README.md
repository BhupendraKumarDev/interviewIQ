# InterviewIQ.AI 🤖💼 — Smart Mock Interview Platform

> **Note on Engineering Background:** This project represents a previous full-stack web engineering milestone developed using the **MERN Stack (MongoDB, Express, React, Node.js)** and **AI API Integration**. My current primary career focus is **Java Full Stack Development (Java, Spring Boot, React, MySQL)**.

[![Live Demo](https://img.shields.io/badge/Demo-Live%20on%20Render-46E3B7?style=for-the-badge&logo=render&logoColor=white)](https://interviewiq-q77q.onrender.com)
[![React](https://img.shields.io/badge/React-19.2-20232A?style=flat-square&logo=react&logoColor=61DAFB)](https://react.dev/)
[![Redux Toolkit](https://img.shields.io/badge/Redux_Toolkit-764ABC?style=flat-square&logo=redux&logoColor=white)](https://redux-toolkit.js.org/)
[![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![Express.js](https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-47A248?style=flat-square&logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![OpenRouter AI](https://img.shields.io/badge/OpenRouter-AI%20API-6366F1?style=flat-square)](https://openrouter.ai/)

---

## 📖 Project Overview

**InterviewIQ.AI** is an advanced, AI-powered smart mock interview platform that simulates real-time technical interviews. By parsing candidate resume documents, the platform automatically generates tailored, role-based technical questions, follows up dynamically on candidate responses, tracks performance scores across sessions, and generates comprehensive analytics reports.

🔗 **Live Deployment:** [https://interviewiq-q77q.onrender.com](https://interviewiq-q77q.onrender.com)

---

## 🚀 Key Features

- **Resume-Driven Mock Interviews:** Upload a professional resume in PDF format to receive custom, contextual technical questions mapped directly to your background and target role.
- **Dynamic Conversational AI:** Powered by **OpenRouter AI**, the system conducts adaptive, multi-turn mock interviews with contextual follow-up questions based on live responses.
- **Interactive Analytics Dashboard:** Monitor overall performance scores out of 10 and view progress metrics over multiple interview sessions using visual data trends.
- **Detailed Evaluation Reports:** Receive objective performance insights mapping specific strengths and growth areas.
- **PDF Report Downloads:** Export structured evaluation sheets directly to local devices for offline review.
- **Credit / Session System:** Tracks candidate interview sessions via an integrated platform credit balance.
- **Secure Authentication:** Robust user authentication featuring Firebase auth integration coupled with standard JWT authorization.

---

## 🛠️ Tech Stack

### Frontend (Client-Side)
- **React.js & Vite** — High-speed module bundling and reactive user interfaces.
- **Redux Toolkit** — Predictable global state management across sessions and interview streams.
- **Tailwind CSS** — Modern, responsive, and minimalist UI system.
- **Chart.js / Recharts** — Dynamic data visualization for tracking user interview performance trends.

### Backend (Server-Side)
- **Node.js & Express.js** — Scalable, decoupled architecture handling API endpoints.
- **OpenRouter AI API** — Orchestrates language model inference for realistic, real-time technical interviewing and performance evaluation.
- **MongoDB & Mongoose** — Document-based data layer maintaining user profiles, transcripts, and evaluation results.
- **Multer** — Middleware handling file memory streams for professional resume PDF uploads.
- **JSON Web Tokens (JWT)** — Custom route protection and user session persistence.

---

## 📂 Project Directory Structure

```text
interviewIQ/
├── server/
│   ├── config/          # Database connections & third-party platform configurations
│   ├── controllers/     # Route handler logic (Auth, Interview streams, Dashboard reports)
│   ├── middlewares/     # isAuth.js (Route protection) & multer.js (PDF file handling)
│   ├── models/          # Mongoose Schemas (User schema, Interview transcript schemas)
│   ├── routes/          # API route routing tables
│   ├── services/        # OpenRouter AI API integration and prompt template engines
│   ├── index.js         # Backend server entry point
│   └── .env             # Server-side secrets and runtime credentials
│
└── client/
    ├── src/
    │   ├── assets/      # Media files, icons, and platform illustrations
    │   ├── components/  # Reusable UI widgets (Charts, Navigation Bars, Modals)
    │   ├── pages/       # Core app views (Home, Interview Page, History, Analytics Dashboard)
    │   ├── redux/       # Store setup, global actions, and state management slices
    │   ├── utils/       # Global formatting functions and firebase.js instance definitions
    │   ├── App.jsx      # Primary component routes root
    │   └── main.jsx     # Frontend runtime mounting setup
    └── .env             # Client-side configuration environment values
```

---

## ⚙️ Installation & Local Setup

### Prerequisites
* Node.js (v18.x or higher)
* MongoDB instance (Local or MongoDB Atlas Cluster)
* OpenRouter AI API Key

### Step-by-Step Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Bhupendra-Kumar-1/interviewIQ.git
   cd interviewIQ
   ```

2. **Configure the Backend Server:**
   ```bash
   cd server
   npm install
   ```
   Create a `.env` file within the `server/` directory:
   ```env
   PORT=5000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_signing_secret
   OPENROUTER_API_KEY=your_openrouter_api_token
   ```
   Start the backend:
   ```bash
   npm run dev
   ```

3. **Configure the Frontend Client:**
   ```bash
   cd ../client
   npm install
   ```
   Create a `.env` file within the `client/` directory:
   ```env
   VITE_BACKEND_URL=http://localhost:5000
   VITE_FIREBASE_API_KEY=your_firebase_configuration_key
   ```
   Launch the development application server:
   ```bash
   npm run dev
   ```

---

## 🛡️ Route Access & Security Middleware

- `isAuth.js`: Prevents unauthorized cross-origin tampering by intercepting requests and parsing JWT auth headers.
- `multer.js`: Isolates file memory streams safely to optimize the parsing of uploaded application files (Resumes).

---

## 📄 License
Distributed under the MIT License.

---

## 👨‍💻 Author
**Bhupendra Kumar**  
- GitHub: [@Bhupendra-Kumar-1](https://github.com/Bhupendra-Kumar-1)  
- LinkedIn: [linkedin.com/in/bhupendra-kumar-dev](https://www.linkedin.com/in/bhupendra-kumar-dev/)

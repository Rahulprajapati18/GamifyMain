# 🎓 Gamify — AI-Powered Gamified Learning Platform

Gamify is an **AI-powered gamified learning platform** designed to make education more interactive, engaging, and accessible. It combines **interactive lessons, quizzes, gamification, AI-powered doubt resolution, progress tracking, multilingual support, and offline-aware progress synchronization** in a single web application.

## 🌐 Live Demo

🚀 **[Visit Gamify Live](gamify-main-ten.vercel.app)**

## 📂 GitHub Repository

🔗 **[View Source Code](https://github.com/Rahulprajapati18/GamifyMain)**

---

## ✨ Key Features

### 🤖 AI-Powered Doubt Assistant
- Integrated **Google Gemini 1.5 Flash** for AI-powered doubt resolution.
- Students can ask questions through an interactive chat interface.
- Includes loading and error handling for API requests.

### 🎮 Gamified Learning
- XP and progress-based learning experience.
- Achievement badges and levels.
- Interactive quizzes and learning activities.
- Visual progress indicators to encourage student engagement.

### 📝 Interactive Quizzes
- Topic-based quizzes with multiple-choice questions.
- Automatic answer evaluation and score calculation.
- Quiz results contribute to student progress.

### 📊 Progress Tracking
- Tracks student learning activity and quiz performance.
- Progress can be stored locally and synchronized with Supabase.
- Teacher dashboard provides an overview of student performance.

### 📡 Offline & Low-Connectivity Support
- Uses browser `localStorage` to temporarily store learning progress.
- Maintains a synchronization queue for unsynced progress.
- Automatically attempts synchronization when internet connectivity returns.

### 🌐 Multilingual Support
- Provides multilingual functionality for improving accessibility.
- Supports multiple Indian languages through the application's translation system.

### 🔐 Authentication
- Email/password authentication using **Supabase Auth**.
- Signup and login form validation.
- Authentication state is managed using React Context.

---

## 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| Frontend | React.js, JavaScript, HTML5, CSS3 |
| Build Tool | Vite |
| Authentication | Supabase Auth |
| Database | Supabase |
| AI | Google Gemini 1.5 Flash |
| Routing | React Router |
| State Management | React Context API |
| Local Storage | Browser localStorage |
| UI & Animation | Framer Motion, Lottie React, tsParticles |
| Version Control | Git, GitHub |
| Deployment | Vercel |

---

## 🏗️ Application Architecture

```text
                         Gamify
                           │
                    React + Vite
                           │
          ┌────────────────┼────────────────┐
          │                │                │
          ▼                ▼                ▼
      Supabase         Gemini API      localStorage
          │                │                │
     Auth + Data       AI Assistant    Offline Queue
          │                                 │
          └──────────── Synchronization ────┘
```

### Main Application Flow

```text
User
 ↓
Login / Signup
 ↓
Supabase Authentication
 ↓
Student Dashboard
 ↓
Lessons / Quizzes
 ↓
Score & Progress
 ↓
Local Storage
 ↓
Synchronization Queue
 ↓
Supabase
```

The AI assistant operates independently through the Gemini API:

```text
Student Question
      ↓
React Chat Interface
      ↓
Gemini API
      ↓
Gemini 1.5 Flash
      ↓
AI Response
      ↓
Chat Interface
```

---

## 📁 Project Structure

```text
GamifyMain/
│
├── public/
│
├── src/
│   ├── components/       # Reusable UI components
│   ├── contexts/         # Authentication, language & progress
│   ├── data/             # Quiz and application data
│   ├── pages/            # Application pages
│   ├── stores/           # Local progress & synchronization
│   ├── supabaseClient.js # Supabase configuration
│   ├── App.jsx           # Application routes
│   └── main.jsx          # Application entry point
│
├── package.json
├── vite.config.js
├── vercel.json
└── README.md
```

---

## 🔑 Main Technologies

### React.js
Used to build the component-based user interface and manage interactive application states.

### Supabase
Used for:
- User authentication
- Cloud data storage
- Student progress synchronization

### Google Gemini
Used to provide the AI-powered doubt resolution feature.

### React Context API
Used for managing application-wide state such as:
- Authentication
- Language
- Student progress

### LocalStorage
Used to retain progress locally and support the application's offline-aware functionality.

### React Router
Used for client-side navigation between lessons, quizzes, dashboard, profile, games, and other application pages.

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Rahulprajapati18/GamifyMain.git
cd GamifyMain
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Create a `.env` file in the project root:

```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

### 4. Start the development server

```bash
npm run dev
```

Open the local URL provided by Vite in your browser.

### 5. Create a production build

```bash
npm run build
```

---

## 🔒 Security Note

For production deployment, sensitive API credentials should never be exposed in client-side code.

The Gemini integration should ideally be moved behind a **secure backend or serverless API endpoint**, keeping the Gemini API key on the server side.

Supabase configuration should be managed through environment variables and appropriate database security policies.

---

## 🔮 Future Improvements

- 🔐 Secure server-side Gemini API integration
- 👥 Stronger role-based access control
- 🛡️ Protected routes
- 📊 Advanced teacher analytics
- 🧠 AI conversation memory and personalized responses
- 🎮 More interactive educational games
- 🌐 Improved internationalization
- 💾 Enhanced offline storage using IndexedDB
- 📈 Personalized learning recommendations

---

## 👨‍💻 Developer

**Rahul Prajapati**

Gamify was developed as an educational project to explore **modern web development, AI integration, cloud authentication, gamification, and offline-aware application design**.

---

⭐ **If you find this project useful, consider giving the repository a star!**

# TripCircle 🌍✈️

TripCircle is a comprehensive trip planning and expense-splitting application. It empowers users to organize group trips, seamlessly track and split expenses, calculate optimal settlements, and leverage AI to plan itineraries. The project is built with a modern MERN stack and incorporates a robust DevOps pipeline.

## 🚀 Features

- **Trip Management:** Create, view, and manage trips with detailed dashboards.
- **Expense Tracking & Splitting:** Add expenses, split them among trip members, and automatically calculate minimal debt settlements (`debtCalculator.js`).
- **AI-Powered Itineraries:** Generate AI trip plans and suggestions.
- **Secure Authentication:** User signup, login, and secure session management.
- **Cloud Media Storage:** Cloudinary integration for uploading receipts or trip photos.
- **Caching:** Redis integration for optimized backend performance.
- **Full CI/CD & DevOps:** Containerized with Docker, automated builds via Jenkins, and code quality checks using SonarQube.

## 🛠️ Tech Stack

### Frontend
- **Framework:** React (built with Vite)
- **State Management:** React Context API (Auth, Theme)
- **Routing & Views:** React Router (Home, Dashboard, Trip Details, Auth)

### Backend
- **Runtime:** Node.js with Express.js
- **Database:** MongoDB (Mongoose for ODM)
- **Caching:** Redis
- **Media Storage:** Cloudinary
- **AI Integration:** Custom AI Controller (for trip planning features)

### DevOps & Infrastructure
- **Containerization:** Docker & Docker Compose
- **CI/CD:** Jenkins (`Jenkinsfile` included)
- **Code Quality:** SonarQube (`sonar-project.properties`)

## 📂 Project Structure

```text
tripcircle-devops/
├── backend/               # Node.js Express server
│   ├── config/            # Database (Mongo, Redis) & Cloudinary configs
│   ├── controllers/       # Route logic (Auth, Trips, Expenses, AI, Settlements)
│   ├── models/            # Mongoose schemas
│   ├── routes/            # Express API routes
│   ├── utils/             # Helper functions (e.g., debt calculator)
│   ├── Dockerfile         # Backend container definition
│   └── sonar-project.properties # SonarQube configuration
├── frontend/              # React application
│   ├── src/
│   │   ├── components/    # Reusable UI components & Modals
│   │   ├── context/       # Auth and Theme context providers
│   │   ├── pages/         # Main views (Home, Dashboard, TripPlanner, etc.)
│   ├── Dockerfile         # Frontend container definition
│   └── vite.config.js     # Vite configuration
├── docker-compose.yml     # Orchestrates frontend, backend, and dependent services
└── Jenkinsfile            # Defines the CI/CD pipeline steps
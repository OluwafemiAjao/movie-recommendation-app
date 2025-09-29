📖 StarFlix – Movie Recommendation App

StarFlix is a full-stack movie recommendation platform built as a capstone project. It allows users to search and discover movies/TV shows (via TMDB API), create accounts, save favorites and watchlists, and manage their profiles — deployed on Vercel (frontend) and Render (backend) with MongoDB Atlas as the database.

🚀 Features
✅ Core (MVP)

User authentication (register, login, JWT-based sessions)

Browse popular movies & TV shows (TMDB API)

Search by title

View detailed movie/TV info (ratings, synopsis, etc.)

Favorites management (add/remove, view list)

Watchlist management (add/remove, view list)

Profile management (view & edit profile, change password)

🎨 UX / Polish

Responsive design (desktop, tablet, mobile)

Loading and error states (spinners / fallback messages)

Fallbacks for missing images or API errors

🌟 Stretch Goals (in progress / optional)

Reviews & ratings

Infinite scroll / pagination

Accessibility improvements (alt text, aria labels)

SEO (meta tags, sitemap, OpenGraph, favicon)

CI/CD & tests (unit, integration, optional e2e)

PWA support

🛠 Tech Stack

Frontend (React + Vite + Tailwind)

React (hooks, context for auth)

React Router (protected routes, navigation)

Axios (TMDB API + backend API)

Tailwind CSS (styling, responsive design)

Backend (Node.js + Express)

Express.js (routes, middleware)

MongoDB Atlas (cloud database)

JWT (authentication & route protection)

Bcrypt (password hashing)

Morgan (logging)

Deployment

Frontend → Vercel

Backend → Render

Database → MongoDB Atlas

📂 Project Structure
starflix/
│
├── backend/                # Express.js backend
│   ├── server.js           # Entry point
│   ├── routes/             # Routes (auth, favorites, watchlist, profile, discover)
│   ├── controllers/        # Controller logic
│   ├── middleware/         # Error handlers, auth middleware
│   ├── models/             # MongoDB models (User, Favorites, etc.)
│   ├── config/             # DB connection
│   └── package.json        
│
├── frontend/               # React frontend
│   ├── src/                
│   │   ├── assets/         # Images, logos, banners
│   │   ├── components/     # UI components (MovieCard, Navbar, etc.)
│   │   ├── pages/          # Pages (Home, Favorites, Profile, Login, etc.)
│   │   ├── services/       # api.js (backend axios wrapper), tmdbService.js
│   │   ├── hooks/          # useAuth, useFavorites, etc.
│   │   ├── App.jsx         
│   │   └── main.jsx        
│   └── package.json
│
├── README.md               # (this file)
└── .env.example            # Example environment variables

⚙️ Environment Variables
Backend (/backend/.env)
PORT=5000
MONGO_URI=<your_mongodb_atlas_connection_string>
JWT_SECRET=<your_jwt_secret>

Frontend (/frontend/.env)
VITE_API_URL=https://your-backend-service.onrender.com/api
VITE_TMDB_API_KEY=<your_tmdb_api_key>

🖥 Local Development

Clone repo

git clone https://github.com/yourusername/starflix.git
cd starflix


Backend setup

cd backend
npm install
npm run dev   # starts backend on http://localhost:5000


Frontend setup

cd frontend
npm install
npm run dev   # starts frontend on http://localhost:5173

🌍 Deployment
Frontend → Vercel

Push repo to GitHub.

Connect GitHub repo to Vercel.

Set frontend environment variables (VITE_API_URL, VITE_TMDB_API_KEY).

Deploy.

Backend → Render

Create new Web Service on Render.

Connect GitHub repo → select backend/.

Set environment variables (PORT, MONGO_URI, JWT_SECRET).

Add build & start commands:

Build: npm install

Start: npm start

🔑 API Endpoints (Backend)

Auth

POST /api/auth/register → Register new user

POST /api/auth/login → Login and get JWT

User

GET /api/users/profile → Get profile (protected)

PUT /api/users/profile → Update profile (protected)

PUT /api/users/change-password → Change password (protected)

Favorites

GET /api/favorites → List favorites

POST /api/favorites/:id → Add favorite

DELETE /api/favorites/:id → Remove favorite

Watchlist

GET /api/watchlist → List watchlist

POST /api/watchlist/:id → Add to watchlist

DELETE /api/watchlist/:id → Remove from watchlist

Discover

GET /api/discover/movies → Popular movies (TMDB)

GET /api/discover/tv → Popular TV shows (TMDB)

🧩 Future Enhancements

Google / social login

Reviews & ratings system

Download/stream functionality

Advanced recommendations (ML-based)

Complete test coverage (unit + e2e)

Accessibility audit

👨‍💻 Author

Capstone project – StarFlix (Movie Recommendation App)

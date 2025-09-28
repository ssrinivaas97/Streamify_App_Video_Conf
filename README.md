# Streamify — Language Exchange (Chat + Video)

A production-ready language exchange platform where users can **chat in real time** and **jump into 1:1 or group video calls** to practice speaking. It includes onboarding, friends/requests, notifications, typing indicators, reactions, threads, image uploads, and multi-theme UI.

## ✨ Highlights

- **Real-time chat**: messages, typing indicators, reactions, threads, image uploads (via Stream Chat).
- **Video calls**: 1:1 & group calls with screen share, reactions, and recording (via Stream Video).
- **Auth + security**: JWT auth stored in HTTP-only cookies, password hashing with bcrypt.
- **Onboarding gate**: Users must complete profile (bio, languages, location) before accessing chat.
- **Friends system**: Send/accept requests; online presence.
- **Modern UI**: React + Vite with 32 themes and clean component patterns.
- **Production-style backend**: Express + MongoDB (Mongoose), layered routes/controllers/models.

## 🧰 Tech Stack

- **Frontend**: React (Vite), TanStack Query, custom hooks.
- **Backend**: Node.js, Express, Mongoose, JWT, bcrypt, dotenv, cookie auth.
- **Realtime/Video**: Stream (Chat & Video SDKs).
- **Database**: MongoDB Atlas.
- **Tooling**: Nodemon, Postman (for API testing).

## 🧩 Key Features → How they’re built

- **Realtime Chat UI** → Stream Chat SDK (threads, reactions, typing status, presence).
- **Video Calling** → Stream Video (1:1/group, screen share, reactions, recordings).
- **Auth** → JWT issued on signup/login, sent as HTTP-only cookie; protected routes middleware.
- **Password Security** → bcrypt pre-save hash in Mongoose model.
- **Onboarding Flow** → `isOnboarded` flag; router guards redirect to onboarding until complete.
- **Friends** → `friends: [ObjectId]` on User; request/accept flows.

To run this app in your system, download the zip file and then extract it. 
Go inside the backend folder and create a .env file locally.
Paste the below variables in it. Make sure you have the API keys.

GET STREAM API KEY HERE -> https://getstream.io/
CREATE MONGO DB CLUSTER -> https://www.mongodb.com/products/platform/atlas-database

Backend ENV File

```
PORT=5001
MONGO_URI=your_mongo_uri
STEAM_API_KEY=your_steam_api_key
STEAM_API_SECRET=your_steam_api_secret
JWT_SECRET_KEY=any random characters
NODE_ENV=development
```

Then Go inside this front end folder.
Create another .env file and paste the Stream API Key there as well.

### Frontend (`/frontend`)

```
VITE_STREAM_API_KEY=your_stream_api_key
```

---

## 🔧 Run the Backend

```bash
cd backend
npm install
npm run dev
```

## 💻 Run the Frontend

```bash
cd frontend
npm install
npm run dev
```

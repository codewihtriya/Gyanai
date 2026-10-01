🚀 GYANAI – AI Powered Chat Application

GYANAI is a full-stack AI chat application inspired by ChatGPT, built with modern web technologies.
It supports real-time AI conversations, JWT authentication, file uploads with AI context, speech-to-text with live mic waveform, code highlighting, and thread-based chat history.
🌐 Live Deployment Links:

🔹 Frontend (Vercel)
👉 https://gyanai-chi.vercel.app/
🔹 Backend (Render)
👉 https://gyanai-backend.onrender.com


✨ Features
🔐 Authentication

User Login & Signup

JWT-based authentication

Protected chat routes

Secure token storage

💬 AI Chat

Real-time AI responses

Thread-based conversation history

Streaming word-by-word replies

Edit previous user messages

Copy AI responses

Text-to-speech for AI replies

📎 File Uploads (ChatGPT-style)

Upload files directly in chat:

PDF

CSV

DOCX

PPT / PPTX

Images (PNG / JPG / JPEG)

Inline file preview inside input box

Image thumbnails

File name chips with remove option

Uploaded files are sent as context to AI

🎤 Voice Input

Speech-to-Text using Web Speech API

Live mic waveform animation

Auto-append voice input to prompt

Smooth mic start/stop handling

🧠 AI Context Handling

User message + file content combined

AI understands uploaded documents & images

Works in both local and production

💻 Code Rendering

Markdown support

Syntax-highlighted code blocks

Dark theme (GitHub Dark)

Inline & block code rendering

🏗️ Tech Stack
Frontend

React (Vite)

React Router

Context API

React Markdown

Highlight.js

Web Speech API

MediaDevices API

CSS (custom UI)

Backend

Node.js

Express.js

MongoDB (Mongoose)

JWT Authentication

Multer (file uploads)

OpenAI API integration

PDF / DOCX / Image parsing

Deployment

Frontend: Vercel

Backend: Render

Database: MongoDB Atlas

🧩 Project Architecture
GYANAI/
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Chat.jsx
│   │   │   ├── ChatWindow.jsx
│   │   │   ├── AuthModal.jsx
│   │   │   ├── Navbar.jsx
│   │   │   └── Sidebar.jsx
│   │   ├── pages/
│   │   │   └── LandingPage.jsx
│   │   ├── MyContext.jsx
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── package.json
│
├── backend/
│   ├── routes/
│   │   ├── auth.js
│   │   └── chat.js
│   ├── models/
│   │   └── Thread.js
│   ├── utils/
│   │   └── openai.js
│   ├── server.js
│   └── package.json
│
└── README.md

⚙️ Environment Variables
Backend (backend/.env)
PORT=3000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
OPENAI_API_KEY=your_openai_api_key

Frontend (frontend/.env)
VITE_API_BASE_URL=http://localhost:3000

▶️ Run Project Locally
1️⃣ Clone Repository
git clone https://github.com/your-username/gyanai.git
cd gyanai

2️⃣ Backend Setup
cd backend
npm install
npm start


Backend will run on:

http://localhost:3000

3️⃣ Frontend Setup
cd frontend
npm install
npm run dev


Frontend will run on:

http://localhost:5173

🔐 Authentication Flow

User logs in or signs up

Backend returns JWT token

Token stored in localStorage 

Protected routes validate token

User redirected to /chat

📤 Chat Flow

User types message / uses mic / uploads file

Frontend sends:

message

threadId

optional file

Backend:

extracts file text (PDF/DOCX/Image OCR)

builds AI prompt

sends to OpenAI

AI response saved in DB

Response streamed to UI

🧪 Tested Scenarios

✔ Login / Signup
✔ Protected routes
✔ File uploads in production
✔ Mic input + waveform
✔ AI replies with code highlighting
✔ Mobile & desktop responsive

🧠 Future Improvements

Chat export (PDF)

Conversation search

Image generation

Multi-language support

Streaming tokens from AI

👨‍💻 Author

Riya garg
Full-Stack Developer | MERN | AI Applications

# 💬 Real-Time Chat App (React + Node.js + Socket.io)

Welcome to the **RoadWare Realtime Chat App** 🚀 — a simple yet powerful full-stack project demonstrating **bi-directional, real-time communication** between users using **Socket.io**.

Built with:
- ⚙️ **Express.js** for backend server
- 🔌 **Socket.io** for real-time WebSocket communication
- ⚛️ **React** for the frontend interface

---

## 🌟 Features

✅ Real-time messaging — no refresh needed  
✅ Join chat with your name  
✅ See messages instantly from all connected users  
✅ System messages for user join/leave events  
✅ Works across multiple browser tabs/windows  

---

## 🧠 Tech Stack

| Layer | Technology |
|--------|-------------|
| Backend | Node.js, Express.js, Socket.io |
| Frontend | React.js, Socket.io Client |
| Styling | Inline CSS |
| Protocol | WebSocket (via Socket.io) |

---


realtime-chat-app/
├── socket-chat-backend/
│ ├── server.js
│ └── package.json
└── socket-chat-frontend/
├── src/
│ ├── components/
│ │ └── Chat.jsx
│ ├── App.js
│ └── index.js
└── package.json

2️⃣ Create server.js and paste backend code
3️⃣ Run the server

node server.js
# Server runs on http://localhost:5000

💻 Frontend Setup (React + Socket.io Client)

1️⃣ Create the React app

npx create-react-app socket-chat-frontend
cd socket-chat-frontend
npm install socket.io-client


2️⃣ Replace App.js and add components/Chat.jsx (from code provided)
3️⃣ Run the frontend

npm start
# React app runs on http://localhost:3000

🧩 How It Works

1️⃣ User joins chat → Enters a name and emits a join event
2️⃣ Server → Stores username and broadcasts a “user joined” system message
3️⃣ Message send → On “Send”, the message is emitted as chatMessage
4️⃣ All clients → Receive and display new message instantly
5️⃣ Disconnect → Server broadcasts “user left” message

🔁 Real-Time Flow Diagram
[React Frontend] --(join/chatMessage)--> [Express + Socket.io Server]
         ^                                      |
         |----(broadcast chat/system msgs)------|

🧪 Testing Steps

✅ Start both frontend and backend servers
✅ Open multiple browser tabs at http://localhost:3000

✅ Join each tab with a different username
✅ Send messages — they’ll appear instantly everywhere
✅ Close a tab — “user left” message appears automatically
## 🏗️ Folder Structure


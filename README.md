
# Zoom Clone - Video Conferencing Application

A full-stack video conferencing application built using the **MERN** stack (MongoDB, Express, React, Node.js), **Socket.io**, and **WebRTC**. This application allows users to create meetings, join via unique URLs, video chat, share screens, and chat in real-time.

## Features

- **Authentication**: Secure Login and Registration system.
- **Video Calls**: Real-time video and audio communication using WebRTC.
- **Screen Sharing**: Ability to share your screen with other participants.
- **Real-time Chat**: In-meeting chat functionality powered by Socket.io.
- **Meeting History**: Track past meetings and rejoin them.
- **Responsive Design**: Built with Material UI for a modern look.

## Tech Stack

- **Frontend**: React.js, Material UI (MUI), Context API
- **Backend**: Node.js, Express.js
- **Database**: MongoDB (Mongoose ODM)
- **Real-time Communication**: Socket.io, WebRTC (Peer-to-Peer)

## Prerequisites

- **Node.js**: Ensure Node.js is installed on your machine.
- **MongoDB**: You need a MongoDB connection string (provided in configuration).

## Installation & Setup

1.  **Clone the repository** (if you haven't already).

2.  **Backend Setup**:
    ```bash
    cd backend
    npm install
    ```
    npm install
    ```
    - Create a `.env` file in the `backend` directory based on `.env.example`.
    - Add your `MONGO_URI` (MongoDB connection string) to the `.env` file.

3.  **Frontend Setup**:
    ```bash
    cd frontend
    npm install
    ```

## Running the Application

To run the application locally, you need to start both the backend and frontend servers.

1.  **Start the Backend**:
    Open a terminal in the `backend` directory:
    ```bash
    npm start
    ```
    *Server will start on `http://localhost:8000`*

2.  **Start the Frontend**:
    Open a valid new terminal in the `frontend` directory:
    ```bash
    npm start
    ```
    *Client will start on `http://localhost:3000`*

## How to Test (Two Users)

Since this is a video calling app, you need two clients to test the connection:

1.  **User A**: Open `http://localhost:3000` in Chrome. Log in or join as guest. Start a meeting.
2.  **User B**: Open an **Incognito Window** or a **different browser** (Firefox/Edge).
3.  **Copy the URL** from User A (e.g., `http://localhost:3000/some-random-id`) and paste it for User B.
4.  User B joins the same room.
5.  You should now see video and audio from both sides!

## Folder Structure

```
/
├── backend/         # Node.js/Express Server
│   ├── src/
│   │   ├── controllers/  # Logic for sockets and users
│   │   ├── models/       # Mongoose Schemas
│   │   ├── routes/       # API Routes
│   │   └── app.js        # Entry point
│   └── ...
├── frontend/        # React Client
│   ├── src/
│   │   ├── pages/        # Application Pages (Landing, Auth, VideoMeet)
│   │   ├── components/   # Reusable components
│   │   ├── contexts/     # Auth Context
│   │   └── ...
│   └── ...
└── README.md
```

## Contributing

Feel free to fork this project and submit pull requests for any enhancements or bug fixes.

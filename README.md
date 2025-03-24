# Real-time Chat Application

A modern, real-time chat application built with Node.js, Express, Socket.IO, and MongoDB. Features include real-time messaging, online status indicators, friend requests, and a responsive design.

## Features

- 🔐 User Authentication
- 💬 Real-time Messaging
- 👥 Friend System
- 🟢 Online/Offline Status
- 📱 Responsive Design
- 🌓 Dark Mode Support
- 🔔 Desktop Notifications
- ⌨️ Keyboard Shortcuts
- 😊 Emoji Support
- 📝 Typing Indicators
- ✓ Read Receipts

## Tech Stack

- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **Backend**: Node.js, Express
- **Database**: MongoDB
- **Real-time Communication**: Socket.IO
- **Authentication**: JWT

## Prerequisites

- Node.js (v14 or higher)
- MongoDB
- npm or yarn

## Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/chat-app.git
cd chat-app
```

2. Install dependencies:

```bash
npm install
```

3. Create a `.env` file in the root directory with the following variables:

```env
PORT=3000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
```

4. Start the server:

```bash
npm start
```

The application will be available at `http://localhost:3000`

## Project Structure

```
chat-app/
├── public/
│   ├── css/
│   ├── js/
│   └── index.html
├── server/
│   ├── config/
│   ├── models/
│   ├── routes/
│   └── server.js
├── .env
├── .gitignore
├── package.json
└── README.md
```

## API Endpoints

### Authentication

- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login user
- `POST /api/auth/logout` - Logout user

### Users

- `GET /api/users/friends` - Get user's friends
- `GET /api/users/friend-requests` - Get pending friend requests
- `POST /api/users/friend-request` - Send friend request
- `PUT /api/users/friend-request/:id` - Respond to friend request
- `GET /api/users/search` - Search for users

### Messages

- `GET /api/messages/:userId` - Get conversation with a user
- `POST /api/messages` - Send a message
- `GET /api/messages/unread` - Get unread message counts

## Socket Events

### Client to Server

- `message:send` - Send a message
- `user:typing` - Send typing indicator
- `message:read` - Send read receipt
- `join:conversation` - Join a conversation room
- `get:status` - Request user statuses

### Server to Client

- `message:new` - New message received
- `message:status` - Message delivery status
- `message:read` - Message read receipt
- `user:typing` - User typing indicator
- `user:status` - User online/offline status

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Socket.IO for real-time communication
- MongoDB for data storage
- Express.js for the web framework

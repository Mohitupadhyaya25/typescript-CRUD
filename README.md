# Express TypeScript API with Sequelize and WebSockets

A robust REST API built with Express, TypeScript, Sequelize ORM, and Socket.IO for real-time communication.

## Features

- JWT authentication with HTTP-only cookies
- Single device session management
- Complete RESTful API endpoints
- Real-time communication with Socket.IO
- MySQL database integration using Sequelize ORM
- Caching for improved performance
- Input validation and error handling
- Rate limiting for security

## Prerequisites

- Node.js (v16 or higher)
- MySQL (v8 or higher)

## Getting Started

1. **Clone the repository**

```bash
git clone <repository-url>
cd express-typescript-api
```

2. **Install dependencies**

```bash
npm install
```

3. **Configure environment variables**

Copy the `.env.example` file to `.env` and update the values:

```bash
cp .env.example .env
```

4. **Create the database**

```sql
CREATE DATABASE express_api_db;
```

5. **Run the development server**

```bash
npm run dev
```

The server will start on port 3000 (or the port specified in your `.env` file).

## Project Structure

```
src/
├── config/           # Configuration files
├── controllers/      # Route handlers
├── middleware/       # Custom middleware
├── models/           # Sequelize models
├── routes/           # Express routes
├── sockets/          # WebSocket implementation
├── tests/            # Test files
├── types/            # TypeScript type definitions
├── utils/            # Helper functions
├── validations/      # Input validation schemas
├── app.ts            # Express app setup
└── server.ts         # Main entry point
```

## API Endpoints

### Authentication

- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login and create a session
- `POST /api/auth/logout` - Logout and invalidate session
- `GET /api/auth/me` - Get authenticated user info

## WebSocket Events

- `join-room` - Join a specific room
- `leave-room` - Leave a specific room
- `send-message` - Send a message to a room
- `new-message` - Receive new messages in a room
- `user-joined` - User joined a room notification
- `user-left` - User left a room notification

## License

MIT
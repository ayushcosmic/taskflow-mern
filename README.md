# TaskFlow — MERN Task Management App

A full-stack task management application built with MongoDB, Express.js, React, and Node.js. Features include user registration and login, JWT-protected routes, personal task CRUD, search and status filters, and dashboard metrics.

## Tech stack
- **Frontend:** React, Vite, React Router, Axios
- **Backend:** Node.js, Express.js, Mongoose
- **Database:** MongoDB
- **Authentication:** JWT and bcryptjs

## Project structure

```text
client/   React + Vite frontend
server/   Express REST API and MongoDB models
```

## Run locally

### Backend
1. Open a terminal in `server/` and run `npm install`.
2. Copy `.env.example` to `.env`.
3. Set `PORT=5000`, `MONGO_URI=mongodb://127.0.0.1:27017/taskflow`, `JWT_SECRET` to a long random secret, and `CLIENT_URL=http://localhost:5173` in `.env`.
4. Run `npm run dev`.

### Frontend
1. Open a second terminal in `client/` and run `npm install`.
2. Run `npm run dev` and open the local Vite URL shown in the terminal.

## API overview
- `POST /api/auth/register` — create an account
- `POST /api/auth/login` — log in
- `GET /api/auth/me` — current authenticated user
- `GET /api/tasks` — list your tasks
- `POST /api/tasks` — create a task
- `PUT/PATCH /api/tasks/:id` — update a task
- `DELETE /api/tasks/:id` — delete a task
- `GET /api/health` — API health check

Task routes require an `Authorization: Bearer <token>` header. Passwords are hashed; never commit `.env` files, real credentials, or production secrets.

## Future improvements
Automated tests, task due dates and priorities, pagination, and a hosted demo with screenshots.

No license has been specified yet.
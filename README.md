# SnapShare

**ARCHIVED** — bootcamp photo-share (milestone-day-35); frozen as-is, not under active development.

Bootcamp photo-sharing app: sign up or Google login, then create posts, comments, likes, and follows. It is not a live-streaming, AI, or TypeScript/Mongo product.

The only published git branch is `milestone-day-35` (GitHub default). There is no `main` branch on the remote.

## What it actually does

- Email/password register and login (JWT)
- Google Sign-In on the frontend
- Posts, comments, likes, and follow/unfollow
- Profile pages and a following feed

## Stack

- Frontend: Create React App (JavaScript), Chakra UI, Tailwind, `@react-oauth/google`
- Backend: Express
- Database: SQLite via Sequelize (not MongoDB)
- Root npm package name: `instagram-webapp`

There is no Socket.io, no TypeScript app code, and no MongoDB.

## Default branch

Clone and check out `milestone-day-35`. Setting `main` as the GitHub default was not possible while that was the only branch.

## Getting started

Prerequisites: Node.js. SQLite is created locally; you do not need MongoDB.

```bash
git clone -b milestone-day-35 https://github.com/HarishKarthickS/SnapShare.git
cd SnapShare
```

Frontend env (Create React App — copy into `frontend/.env`):

```bash
cp .env.example frontend/.env
```

Set `REACT_APP_GOOGLE_CLIENT_ID` to your Google OAuth web client ID. Do not commit real client IDs.

Backend env (copy into `backend/.env`):

```
JWT_SECRET=change-me
```

Install and run (root scripts, two terminals):

```bash
npm run frontend
npm run backend
```

The backend script downloads a sample SQLite file into `backend/data/` and starts Express on port 5000. The frontend is `react-scripts start` (typically port 3000). There is no `npm run dev` at the repo root.

## License

See the repository for license details if a LICENSE file is present.

# Career LaunchPad — Employee CRUD Application

A small full-stack CRUD application for managing user records.

## Features
- List users
- Create a user
- Update a user by ID
- Delete a user by ID
- Express API with parameterized PostgreSQL queries

## Stack
- Node.js and Express
- PostgreSQL with pg
- dotenv and CORS
- JavaScript frontend

## Project Structure
```text
backend/
  server.js
frontend/
  app.js
```

## Setup
1. Install Node.js and PostgreSQL.
2. Create a PostgreSQL database named career_launchpad and a users table with id, name, and email columns.
3. Configure these environment variables in a local .env file inside backend/:

```env
DB_HOST=localhost
DB_USER=postgres
DB_PASSWORD=your_local_database_password
DB_NAME=career_launchpad
DB_PORT=5432
PORT=3000
```

4. Install and start the backend:
```bash
cd backend
npm install
node server.js
```

5. Serve the frontend files locally and configure the API base URL to point to the backend.

## API
| Method | Endpoint | Purpose |
|---|---|---|
| GET | /users | List users |
| POST | /users | Create a user |
| PUT | /users/:id | Update a user |
| DELETE | /users/:id | Delete a user |

## Security
- Database credentials must stay in environment variables and must never be committed.
- Use a restricted database account rather than a superuser in deployed environments.
- Add input validation, authentication, and authorization before exposing the API publicly.
- If a real credential was ever committed, rotate it; deleting it from the latest file does not remove it from Git history.
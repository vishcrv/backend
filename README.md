# Node.js Todo App (JWT, SQLite, Express)

A simple authentication-protected Todo App using Node.js, Express, SQLite, and JWT.

## Features

- User registration and login (JWT authentication)
- CRUD operations for todos (protected routes)
- SQLite in-memory database
- REST client file for easy API testing

## Setup

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Configure environment variables:**
   - Copy `.env.example` to `.env` and set your secrets (see below).

3. **Run the server:**
   ```bash
   npm run dev
   ```
   or
   ```bash
   node --env-file=.env --experimental-sqlite ./src/server.js
   ```

4. **Test the API:**
   - Use the provided `todo-app.rest` file with the [REST Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client) extension in VS Code.

## Environment Variables

Create a `.env` file in the root:

```
JWT_SECRET=your_jwt_secret_key
PORT=5006
```

## REST Client Usage

- Replace `@token` in `todo-app.rest` with your JWT token after login.
- Run requests directly in VS Code using the REST Client extension.

## Project Structure

```
public/
  index.html
  styles.css
src/
  db.js
  server.js
  middleware/
    authMiddleware.js
  routes/
    authRoutes.js
    todoRoutes.js
.env
.gitignore
package.json
todo-app.rest
README.md
```


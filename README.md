basic jwt-auth todo app using node.js, express, and sqlite with protected crud routes.

### features

- user registration and login (jwt auth)
- crud operations for todos (protected routes)
- sqLite in-memory database
- rest client file for easy api testing

### setup

1. **install dependencies:**
   ```bash
   npm install
   ```

2. **configure env var:**
   - Copy `.env.example` to `.env` and set your secrets (see below).

3. **run the server:**
   ```bash
   npm run dev
   ```
   or
   ```bash
   node --env-file=.env --experimental-sqlite ./src/server.js
   ```

4. **test the api:**
   - use the provided `todo-app.rest` file with the [REST Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client) extension in VS Code.

### env variables

create a `.env` file in the root:

```
JWT_SECRET=your_jwt_secret_key
PORT=5006
```

### rest client usage

- replace `@token` in `todo-app.rest` with your JWT token after login.
- run requests directly in VS Code using the REST Client extension.




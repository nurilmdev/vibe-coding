# Vibe-Code Project

This project is a new Node.js application built with TypeScript, Elysia JS, Drizzle ORM, and PostgreSQL.

## Setup Instructions

1.  **Clone the repository (if not already done):**

    ```bash
    git clone [repository-url]
    cd vibe-code
    ```

2.  **Install dependencies:**

    ```bash
    npm install
    ```

3.  **Configure environment variables:**
    Create a `.env` file in the root directory and add your PostgreSQL connection string:

    ```
    DATABASE_URL="postgresql://user:password@localhost:5432/database_name"
    ```

    _Make sure to replace `user`, `password`, `localhost:5432`, and `database_name` with your actual PostgreSQL credentials._

4.  **Run migrations (if any):**
    _This project uses Drizzle ORM. You might need to run migrations to set up your database schema._
    (Instructions for Drizzle migrations would go here once a `drizzle.config.ts` is created and migrations are generated.)

5.  **Build the project:**

    ```bash
    npm run build
    ```

    _You may need to add a build script to `package.json` for `tsc`._

6.  **Start the development server:**
    ```bash
    npm start
    ```
    _You may need to add a start script to `package.json`._

## Project Structure

- `src/index.ts`: Main application entry point with Elysia routes.
- `src/db/`: Contains database schema (`schema.ts`) and Drizzle client configuration (`index.ts`).
- `src/routes/`: (Future) Dedicated directory for organizing API routes.
- `tsconfig.json`: TypeScript configuration.
- `.env`: Environment variables (e.g., database connection string).
- `.gitignore`: Specifies intentionally untracked files to ignore.

## Implemented Functionality

- **Root endpoint (`/`):** Returns "Hello Elysia!".
- **Users endpoint (`/users`):** Fetches all users from the PostgreSQL database using Drizzle ORM.

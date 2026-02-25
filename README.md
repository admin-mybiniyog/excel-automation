# excel-automation

A full-stack web platform for **Excel-style financial analysis and signal generation**.  
It combines a rich spreadsheet-like UI with a TypeScript/Express backend, PostgreSQL, and a custom formula engine to help you build, evaluate, and monitor investment signals at scale.

## Features

- **Excel-like formulas**: Define and evaluate formulas over company financials, quarters, and custom metrics.
- **Interactive web UI**: Modern React + Tailwind + shadcn/ui interface with dashboards, company views, and spreadsheets.
- **Signals engine**: Generate BUY/HOLD/SELL (and other) signals based on your formulas and thresholds.
- **User & role management**: Multi-user system with roles, permissions, and 2‑step login via OTP.
- **Scheduling & scraping**: Background tasks for scraping data, updating sectors, and recalculating signals.
- **PostgreSQL + Drizzle ORM**: Strongly-typed schema and migrations for reliable data management.

## Tech Stack

- **Frontend**: React 18, TypeScript, Vite, Tailwind CSS, shadcn/ui, Radix UI, React Query.
- **Backend**: Node.js, TypeScript, Express, Drizzle ORM, PostgreSQL.
- **Tooling**: Playwright (tests), esbuild, tsx, drizzle-kit.

## Getting Started

1. **Install dependencies**

   ```bash
   npm install
   ```

2. **Configure environment**

   Create a `.env` file in the project root and set at least:

   ```bash
   DATABASE_URL=postgresql://user:password@host:5432/database?sslmode=require
   PORT=5000
   NODE_ENV=development
   ```

   For detailed environment and infrastructure options, see `SETUP.md`.

3. **Run database migrations**

   ```bash
   npm run db:push
   ```

4. **Start the app in development mode**

   ```bash
   npm run dev
   ```

   The server will start on the port specified in `PORT` (default: `5000`).

## Production Build

```bash
npm run build
npm start
```

This will bundle the backend and frontend and start the production server.

## Useful Scripts

- `npm run dev` – Start the backend in development mode.
- `npm run build` – Build frontend and backend bundles.
- `npm start` – Run the production server.
- `npm run db:push` – Apply database schema migrations using drizzle-kit.
- `npm test` – Run Playwright tests.

## Additional Documentation

- `SETUP.md` – Detailed setup and deployment instructions.
- `MIGRATION_GUIDE.md` – Notes on data/schema migrations.
- `EXCEL_FORMULA_GUIDE.md` – Details about supported Excel-style formulas.
- `LOG_VIEWING_GUIDE.md` – How to view and interpret system logs.
- `FIX_HOLD_SIGNAL_ISSUE.md` – Internal notes on signal issues and fixes.


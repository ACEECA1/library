# Digital Library

A lightweight, fully-featured digital library platform for managing, reading, and organizing PDF books online. Built to be modular, fast, and easy to deploy.

## Features
- **In-Browser Reading:** Read PDFs directly in the browser with text-selection enabled and downloads restricted. Remembers your last read page automatically.
- **Admin Dashboard:** Role-based access control. Admins can upload books, moderate comments, manage users, and issue bans/timeouts.
- **Organization:** Categorize books by series, tags, and categories.
- **Bookmarks & Collections:** Users can bookmark their favorite books to easily find them later.
- **Localization:** Built-in multi-language support (i18n).

## Tech Stack
**Frontend:**
- React (Vite)
- TypeScript
- Tailwind CSS
- React-PDF (for rendering books without exposing the raw file)
- React-i18next (localization)

**Backend:**
- Java & Spring Boot
- Spring Security (JWT authentication)
- Elasticsearch (for fast full-text searching)

## Getting Started

### 1. Clone the repository
Since the frontend and backend are kept in separate git submodules, you need to use the `--recurse-submodules` flag when cloning:

```bash
git clone --recurse-submodules https://github.com/ACEECA1/library.git
cd library
```

*If you already cloned without the flag, you can initialize the submodules manually by running:*
```bash
git submodule update --init --recursive
```

### 2. Environment Variables
Make sure to configure your `.env` file in the root directory before spinning up the containers. You can copy the provided example file if there is one, or fill in the necessary database and Elasticsearch credentials.

### 3. Run with Docker
The easiest way to run the entire stack (Database, Elasticsearch, Backend API, and Frontend) is via Docker Compose.

```bash
docker-compose up --build -d
```

Once everything is up and running, you can access the frontend at `http://localhost:5173` (or whatever port you configured) and the API at `http://localhost:8080`.

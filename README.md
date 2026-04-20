# Visual Search Application

A full-stack application for visual search capabilities, built with Next.js frontend and FastAPI backend.

## Quick Start

### Prerequisites

- Docker
- Docker Compose

### Running the Application

1. Clone the repository
2. From the root directory, run:

```bash
docker-compose up --build
```

This will start both the frontend and backend services:

- Frontend: http://localhost:3000
- Backend API: http://localhost:8000

## Development Setup

### Frontend (Next.js)

For local development of the frontend:

1. Navigate to the frontend directory:

```bash
cd frontend
```

2. Install dependencies:

```bash
npm install
```

3. Start the development server:

```bash
npm run dev
```

### Backend (FastAPI)

For local development of the backend:

1. Create and activate a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: venv\Scripts\activate
```

2. Navigate to the backend directory:

```bash
cd backend
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Start the development server:

```bash
uvicorn main:app --reload
```

## Architecture

- Frontend: Next.js application with TypeScript
- Backend: FastAPI application with Python
- Image Processing: PyTorch, OpenCV, and Transformers
- API Documentation: Swagger UI and ReDoc

## Deployment

### Frontend (Vercel / Netlify)

The project includes `vercel.json` and `netlify.toml` in the root directory to handle the subdirectory structure.

1.  Push your code to GitHub.
2.  Connect your repository to Vercel or Netlify.
3.  **Important:** In the deployment settings, ensure the **Root Directory** is set to `frontend`.
4.  Add an environment variable `NEXT_PUBLIC_API_URL` pointing to your deployed backend URL.

### Backend

The backend is a FastAPI application that should be deployed to a service supporting Python/Docker (e.g., Render, Railway, or Fly.io).

1.  Use the provided `backend/Dockerfile` for deployment.
2.  Ensure the `API_URL` in the frontend matches the deployed backend URL.

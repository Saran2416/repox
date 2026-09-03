# Setup

## Prerequisites

- Node.js 20+
- Python 3.11+
- Git

## Backend

```bash
cd Backend
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
cp .env.example .env
python -m uvicorn main:app --reload --port 8000
```

Required environment variables in `Backend/.env`:

- `GITHUB_CLIENT_ID`
- `GITHUB_CLIENT_SECRET`
- `GITHUB_CALLBACK_URL` (default: `http://localhost:8000/auth/github/callback`)
- `FRONTEND_URL` (default: `http://localhost:5173`)
- `OPENROUTER_API_KEY`
- `OPENROUTER_MODEL`

## Frontend

```bash
cd frontend
npm install
npm run dev
```

By default the frontend expects backend on `http://localhost:8000`.

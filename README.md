# Next.js + FastAPI Services Monorepo

Minimal example showing Vercel Services with:

- `frontend` (Next.js) mounted at `/`
- `backend` (FastAPI) mounted at `/svc/api`

It demonstrates:

1. A **Next.js API route** at `/api/hello`
2. A **FastAPI backend route** at `/svc/api/status`
3. **Backend mounting via service routePrefix** in `vercel.json`

## Project structure

```txt
next-fastapi-monorepo/
├── backend/
│   ├── main.py
│   └── pyproject.toml
├── frontend/
│   ├── app/
│   │   ├── api/hello/route.js
│   │   ├── globals.css
│   │   ├── layout.js
│   │   └── page.js
│   └── package.json
└── vercel.json
```

## Services config

`vercel.json` uses `experimentalServices` to mount both services:

- `frontend` at `/`
- `backend` at `/svc/api`

## Run locally

Install frontend dependencies:

```bash
cd frontend
npm install
```

Then run all services via Vercel local runtime:

```bash
cd ..
vercel dev -L
```

Open `http://localhost:3000` and try:

- `/api/hello` (Next.js API route)
- `/svc/api/status` (FastAPI route)
- `/svc/api/docs` (FastAPI Swagger UI)
# vercel-services-next-fastapi-monorepo-example

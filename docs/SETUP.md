# Setup

## Prerequisites
- Python 3.11+
- Node 20+
- `uv`
- `pnpm`
- Docker (optional)
- Terraform + Azure CLI + azd (for cloud deploy)

## Backend
```bash
cd py/apps/app-template
uv pip install -e .[dev]
uv run uvicorn main:app --reload --port 8001
```

## Frontend
```bash
cd ts
pnpm install
pnpm --filter ui-copilot-template dev
```

## Local E2E (Docker)
```bash
docker compose up --build
```

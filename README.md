# First FastAPI API

This repo hosts a minimal FastAPI application based on the official quick-start tutorial.

## Getting Started

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install "fastapi[standard]"
```

## Running the Server

```bash
uvicorn main:app --reload
```

Once running:

- `GET /` returns a simple Hello World response.
- `GET /items/{item_id}?q=foo` echoes the item ID and optional query string.
- `POST /items/` accepts a JSON body and responds with the submitted payload.

Interactive API docs live at http://127.0.0.1:8000/docs when the server is running. Stop the server any time with `Ctrl+C`.

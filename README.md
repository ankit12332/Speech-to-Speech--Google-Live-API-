# First FastAPI API

This repo hosts a minimal FastAPI application based on the official quick-start tutorial.

## Getting Started

### 1. Create and Activate Virtual Environment

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
```

### 2. Install Dependencies

The `requirements.txt` file contains `fastapi[standard]` and `python-dotenv`. The `fastapi[standard]` bundle includes useful extras such as `uvicorn` and `pydantic`.

```bash
pip install -r requirements.txt
```

**Alternatively**, if you prefer to install dependencies manually:

```bash
pip install "fastapi[standard]" python-dotenv
```

### 3. Updating Dependencies

When you add or upgrade dependencies inside the virtual environment, capture the new versions with:

```bash
pip freeze > requirements.txt
```

Then commit the updated `requirements.txt` so collaborators can reproduce the same environment.

## Running the Server

```bash
uvicorn main:app --reload
```

Once running:

- `GET /` returns `{"Hello": "World"}`.
- `GET /items/{item_id}` returns `{"item_id": <int>, "q": <str|null>}`, mirroring the path parameter and the optional `q` query string if it is present (e.g., `/items/3?q=foo`).

Interactive API docs live at http://127.0.0.1:8000/docs when the server is running. Stop the server any time with `Ctrl+C`.

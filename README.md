# DevOps Demo Application

A beginner-friendly Flask application that will gradually become a complete DevOps project.

## Run locally with Python

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

Open http://localhost:5000 and http://localhost:5000/health.

Run tests with:

```bash
pytest
```

## Run with Docker

```bash
docker build -t devops-demo:1.0 .
docker run --rm -p 5000:5000 devops-demo:1.0
```

Then open http://localhost:5000/health.

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

## Run with Kubernetes and Minikube

Start Minikube and make the local Docker image available to it:

```bash
minikube start
minikube image load devops-demo:1.0
```

Deploy the application and check its resources:

```bash
kubectl apply -f k8s/
kubectl get pods
kubectl get services
```

Open the service in your browser:

```bash
minikube service devops-demo
```

Clean up the Kubernetes resources when finished:

```bash
kubectl delete -f k8s/
```

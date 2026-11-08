# Production-Ready Containerized AI Inference Service

A production-grade Proof-of-Concept (PoC) microservice that bridges offline machine learning models and online production environments using FastAPI, Pydantic, and Docker.

---

## 🚀 Key Features
* **FastAPI Backend:** High-performance asynchronous API serving real-time predictions.
* **Strict Schema Validation:** Powered by Pydantic models for automated type enforcement and error handling (`422 Unprocessable Entity`).
* **Containerized Runtime:** Fully isolated inside a multi-layered Docker image (`ai-model-service:v1`) built on Python 3.10 slim.
* **Custom Observability Middleware:** Intercepts HTTP traffic to track request paths, methods, status codes, and execution latencies down to the millisecond.
* **Health Probes:** Built-in liveness endpoint (`/health`) for container orchestrator monitoring.

---

## 📂 Project Structure
```text
ai-deployment-project/
├── app/
│   └── main.py          # FastAPI application logic & middleware
├── Dockerfile           # Multi-layered container build instructions
├── requirements.txt     # Explicit dependency lockfile
└── README.md            # Project documentation

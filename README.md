# Alzheimer's MRI Analysis System

An end-to-end web application for MRI image analysis using **FastAPI**, **PyTorch**, **Logistic Regression**, and **Docker**. The system allows users to upload MRI images through a web interface and obtain predictions from multiple machine learning models through REST APIs.

---

## Overview

This project was developed as part of a Computer Science senior design project. The application integrates machine learning models with a web-based interface to demonstrate automated MRI image analysis. The backend is built using FastAPI microservices, while the frontend provides an intuitive interface for uploading MRI images and viewing prediction results.

The system supports multiple machine learning models and is containerized using Docker for easy deployment.

---

## Features

- Web-based MRI image upload
- FastAPI REST APIs
- PyTorch CNN inference service
- Logistic Regression inference service
- Dockerized microservice architecture
- Load balancing support
- Confidence score prediction
- Adjustable prediction threshold
- Health check endpoints

---

## Project Structure

```
alzheimers-mri-analysis/
│
├── frontend/                # HTML, CSS and JavaScript frontend
├── service_CNN/             # PyTorch CNN prediction service
├── service_LR/              # Logistic Regression prediction service
├── load_balancer/           # Load balancing service
├── docker-compose.yml       # Docker Compose configuration
├── .gitignore
└── README.md
```

---

## Technologies Used

- Python
- FastAPI
- PyTorch
- Scikit-learn
- Docker
- HTML
- CSS
- JavaScript
- NumPy
- Pillow

---

## System Architecture

```
Frontend
      │
      ▼
Load Balancer
      │
 ┌──────────────┐
 │              │
 ▼              ▼
CNN Service   Logistic Regression Service
      │              │
      └──────┬───────┘
             ▼
      Prediction Response
```

---

## API Endpoints

### CNN Service

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | `/` | Service status |
| GET | `/health` | Health check |
| POST | `/predict` | Predict from MRI image |
| POST | `/predict_threshold` | Predict using a custom threshold |

### Logistic Regression Service

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | `/` | Service status |
| GET | `/health` | Health check |
| POST | `/predict` | Predict from MRI image |
| POST | `/predict_threshold` | Predict using a custom threshold |

---

## Running the Project

Clone the repository:

```bash
git clone https://github.com/Jafin-Khan/alzheimers-mri-analysis.git
```

Navigate to the project directory:

```bash
cd alzheimers-mri-analysis
```

Start all services:

```bash
docker-compose up --build
```

---

## Research and Educational Purpose

This repository demonstrates the integration of machine learning models into a deployable web application for educational and research purposes. It showcases the use of modern software engineering practices, including microservices, REST APIs, Docker-based deployment, and machine learning inference.

---

## Future Improvements

- Add additional deep learning architectures
- Improve model accuracy using larger datasets
- Add user authentication
- Deploy to a cloud platform
- Implement automated testing and CI/CD

---

## Author

**Jafin Khan**

Bachelor of Science in Computer Science  
Prairie View A&M University

LinkedIn: https://www.linkedin.com/in/jafin-khan-188a12250/

---

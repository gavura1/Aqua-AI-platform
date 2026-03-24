# Aqua AI Platform

AI-driven platform for swimming facility analytics, focused on visitor traffic prediction, course recommendation, and anomaly detection.

---

## About the Project

Aqua AI Platform is a system design and ongoing implementation of an intelligent solution for managing and optimizing swimming facility operations using artificial intelligence.

The project is based on a real-world use case for an actual swimming facility. Due to confidentiality and data protection requirements, certain names, identifiers, and parts of the dataset have been anonymized or modified.

The system is designed as a standalone module that can be integrated into an existing web portal via a REST API.

---

## Project Goals

The main objective of the project is to develop an intelligent system that:

- predicts visitor traffic on an hourly basis (7 days ahead),
- recommends suitable courses based on user preferences,
- detects anomalies (significant deviations between predicted and actual attendance),
- provides data-driven insights for operational decision-making.

The goal is to improve both operational efficiency and user experience.

---

## Data

The project works with real-world data obtained from swimming facility operations. The data has been:

- anonymized,
- adapted for public use,
- aggregated (no personally identifiable information included).

Using real data allows the models to capture realistic patterns such as weekends, seasonality, and peak hours.

---

## AI Components

The system includes three main AI components:

### 1. Visitor Traffic Prediction
- time series regression problem
- model: RandomForestRegressor
- output: hourly prediction for 7 days (168 hours)

### 2. Course Recommendation
- classification problem
- model: RandomForestClassifier
- inputs: age, skill level, time availability
- output: top 3 recommended courses

### 3. Anomaly Detection
- model: Isolation Forest
- detects significant deviations between predicted and actual attendance

---

## System Architecture

The system is designed using a three-tier architecture:

- **Presentation Layer** – web interface (frontend)
- **Application Layer** – REST API + AI modules (FastAPI)
- **Data Layer** – PostgreSQL database

This architecture ensures:
- separation of concerns,
- maintainability,
- scalability.

---

## Deployment and Technologies

The system is designed for deployment in a cloud environment:

- Docker – containerization
- AWS (EC2 / ECS / RDS) – hosting
- GitHub Actions – CI/CD pipeline
- Prometheus + Grafana – monitoring
- AWS CloudWatch – logging

---

## Current Status

🔧 The project is currently in the system design phase.

This version includes:
- complete system design documentation,
- architecture design,
- requirements specification,
- AI component design,
- test case design,
- deployment strategy.

Backend implementation and model development are planned as the next phase.

---

## Future Work

Planned extensions include:

- backend implementation (FastAPI),
- training and deployment of AI models,
- integration with a real web portal,
- real-time data processing,
- advanced monitoring and alerting.

---

## Documentation

The complete system design documentation is available in:

👉 `SYSTEM_DESIGN_DOCUMENTATION.pdf`

---

## Disclaimer

This project is based on a real-world use case. The publicly available version has been modified to ensure data privacy and confidentiality.

---

## Author

Vladimír Gavura

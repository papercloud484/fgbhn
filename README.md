# SurakshaPay

**Intelligent Parametric Income Protection for the Gig Economy**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Architecture: Event-Driven](https://img.shields.io/badge/Architecture-Event--Driven-blue)](#system-architecture)
[![Cloud: AWS](https://img.shields.io/badge/Cloud-AWS-232F3E?logo=amazonaws)](#tech-stack)
[![Frontend: Next.js](https://img.shields.io/badge/Frontend-Next.js-black?logo=nextdotjs)](#tech-stack)
[![Mobile: Flutter](https://img.shields.io/badge/Mobile-Flutter-02569B?logo=flutter)](#tech-stack)
[![Backend: NestJS](https://img.shields.io/badge/Backend-NestJS-E0234E?logo=nestjs)](#tech-stack)
[![API: FastAPI](https://img.shields.io/badge/API-FastAPI-009688?logo=fastapi)](#tech-stack)
[![Runtime: Node.js](https://img.shields.io/badge/Runtime-Node.js-339933?logo=nodedotjs)](#tech-stack)
[![Language: Python](https://img.shields.io/badge/Language-Python-3776AB?logo=python)](#tech-stack)
[![Messaging: Kafka](https://img.shields.io/badge/Messaging-Kafka-231F20?logo=apachekafka)](#tech-stack)
[![Messaging: RabbitMQ](https://img.shields.io/badge/Messaging-RabbitMQ-FF6600?logo=rabbitmq)](#tech-stack)
[![Database: MySQL](https://img.shields.io/badge/Database-MySQL-4479A1?logo=mysql)](#tech-stack)
[![Cache: Redis](https://img.shields.io/badge/Cache-Redis-DC382D?logo=redis)](#tech-stack)
[![Container: Docker](https://img.shields.io/badge/Container-Docker-2496ED?logo=docker)](#tech-stack)
[![CI/CD: GitHub Actions](https://img.shields.io/badge/CI/CD-GitHub_Actions-2088FF?logo=githubactions)](#tech-stack)
[![Monitoring: Prometheus](https://img.shields.io/badge/Monitoring-Prometheus-E6522C?logo=prometheus)](#tech-stack)
[![Dashboards: Grafana](https://img.shields.io/badge/Dashboards-Grafana-F46800?logo=grafana)](#tech-stack)
[![ML: Enabled](https://img.shields.io/badge/ML-Risk%20Scoring%20%26%20Pricing-purple)](#intelligence-layer)
[![Status: Active Development](https://img.shields.io/badge/Status-Active_Development-brightgreen)](#roadmap)

> **SurakshaPay is a real-time, AI-assisted parametric insurance system that protects gig workers from sudden income loss caused by extreme weather, hazardous air quality, civic restrictions, and operational disruptions.**

---

## Why SurakshaPay

Gig workers earn daily, but they also face daily risk.

A delivery partner can lose an entire shift's income because of heavy rainfall, extreme heat, toxic air, curfews, or city-level shutdowns. Traditional insurance is too slow, too manual, and too claim-heavy for this reality.

**SurakshaPay flips the model.**  
Instead of waiting for a worker to file a claim, the system continuously monitors verified disruption signals and automatically releases compensation when predefined trigger conditions are met.

### In one line

**If a disruption happens, the system detects it, validates it, and settles support automatically.**

---

## Problem Statement

India’s gig economy depends on delivery workers, riders, and field agents who operate in uncertain conditions with little to no localized income protection.

Current challenges include:

- No fast, automated safety net for short-term income disruption.
- Claims-based insurance is too slow for workers who depend on daily cash flow.
- Risk is hyperlocal, but existing financial products are generalized.
- Fraud risk is high if settlement systems rely only on self-reported claims or naive GPS data.
- Platforms need a scalable, low-friction, rule-based mechanism for emergency worker support.

---

## Solution Overview

SurakshaPay is a **parametric protection engine** for gig workers.

It combines:

- Real-time environmental and municipal data.
- Platform telemetry such as order volume and worker activity.
- Machine learning for risk scoring, pricing, and anomaly detection.
- A deterministic rules engine for payout execution.
- Zero-trust validation to reduce spoofing and abuse.

### Core promise

- **No manual claims**
- **No long approval queues**
- **No ambiguity in payout conditions**
- **Fast, explainable, event-driven settlement**

---

## Key Features

- **Parametric insurance logic** based on verified trigger conditions.
- **Instant settlement workflow** for trusted cases.
- **Micro-premium model** deducted from worker earnings or platform-led wallets.
- **ML-powered disruption forecasting** for weather, AQI, and demand collapse scenarios.
- **Dynamic premium pricing** based on volatility and regional exposure.
- **Fraud-resistant trust engine** using multi-signal validation.
- **Event-driven microservices architecture** for scale and fault isolation.
- **Admin dashboard** for monitoring risk, triggers, payouts, and anomalies.
- **Audit-friendly decision trail** for every settlement action.

---
## System Architecture


SurakshaPay is designed as an **event-driven microservices system** with loosely coupled services for ingestion, intelligence, decisioning, and payout execution.

### Architecture Diagram

![System Architecture Overview](./assets/architecture_flow.png)


### Engineering Characteristics

- **Asynchronous event processing** for high throughput.
- **Loose coupling** between services for easier scaling and maintenance.
- **Replayable event streams** for audit and recovery.
- **Fault-tolerant workflow design** using queues, retries, and dead-letter patterns.
- **Fast-path settlement** for high-confidence cases.

---

## User Flow

The worker's journey from enrollment to automated support release follows a seamless, trust-verified cycle.

![User Flow Journey](./assets/user_flow.png)


---

## Intelligence Layer

SurakshaPay separates intelligence workloads into focused pipelines so each component can evolve independently.

### Intelligence Matrix

| Pipeline | Purpose | Possible Models | Inputs / Signals | Outputs |
| --- | --- | --- | --- | --- |
| Risk Profiling | Predict disruption likelihood for worker or region | Random Forest, XGBoost, Gradient Boosting | Rainfall intensity, temperature severity, AQI, order volume change, worker activity, geo-tagged disruptions | Risk score, disruption probability, confidence band, region classification |
| Dynamic Pricing | Compute personalized or region-aware premium ranges | Linear Regression, Regularized Regression, volatility heuristics | Historical earning loss, claim-frequency equivalents, coverage tier, regional risk, seasonal instability | Premium range and pricing recommendation |
| Spatial Forecasting | Detect geographic clusters where disruptions are emerging | K-Means, DBSCAN, ARIMA, geo-temporal clustering | Regional geo-temporal events and operations data | Emerging risk zones and regional alerts |
| Anomaly Detection | Identify suspicious behavior or manipulated telemetry | Isolation Forest, Local Outlier Factor, threshold heuristics | Kinematic patterns, network behavior, payout sequences | Anomaly score and fraud risk flag |

### Continuous Retraining

Model quality is continuously improved using:
- Settlement outcomes
- False-positive review data
- Regional drift trends
- Trigger performance analytics

---

## Deterministic Actuarial Logic

Premiums are computed dynamically based on expected worker loss, disruption probability, and historical volatility.

\[
P_w = (L_w \times p \times \alpha) + (\sigma \times \beta) + M
\]

Where:

| Symbol | Meaning |
| --- | --- |
| \(P_w\) | Worker-specific premium |
| \(L_w\) | Expected weekly income deficit |
| \(p\) | Disruption probability |
| \(\alpha\) | Coverage factor |
| \(\sigma\) | Historical volatility coefficient |
| \(\beta\) | Sensitivity calibration factor |
| \(M\) | Platform buffer or operational margin |

### Design Principles

- Pricing must be **bounded**
- Pricing must be **explainable**
- Pricing must be **reproducible**
- Payouts must remain **solvency-aware**
- Fallback rules should exist if ML services degrade

---

## Zero-Trust Fraud Defense

A core challenge in parametric payout systems is preventing spoofed triggers and fake eligibility. SurakshaPay uses a **multi-signal trust engine** instead of relying on a single weak signal like raw GPS.

### Trust Signals

| Signal | Validation Objective |
| --- | --- |
| Kinematic verification | Confirms movement patterns match plausible delivery behavior |
| Lifecycle consistency | Validates event order such as accept \(\rightarrow\) pickup \(\rightarrow\) drop |
| Network integrity | Cross-checks IP behavior, carrier shifts, and session consistency |
| Behavioral anomaly analysis | Flags repetitive suspicious payout patterns |
| Geo-context validation | Compares worker state against regional disruption evidence |
| Graceful edge-case handling | Avoids penalizing legitimate low-battery or weak-network sessions |

### Trust Score Policy

| Trust Score Band | Decision Path |
| --- | --- |
| \(\ge 70\) | Fast-track payout |
| \(40\) to \(69\) | Conditional review path |
| \(< 40\) | Audit queue and secondary validation |

---

## Parametric Trigger Engine

Payouts are not manually approved. They are executed when deterministic conditions are met.

### Example Trigger Logic

```python
def evaluate_and_settle(environmental_api, platform_telemetry, user_id, coverage_tier):
    if (
        environmental_api.rainfall_mm_3hr > 60.0
        and platform_telemetry.order_volume_drop >= 0.50
    ):
        execute_settlement(user_id, coverage_tier)

    elif (
        environmental_api.temperature_c >= 45.0
        and platform_telemetry.worker_uptime_drop >= 0.40
    ):
        execute_settlement(user_id, coverage_tier)

    elif (
        environmental_api.aqi >= 450
        and platform_telemetry.outdoor_ops_halted is True
    ):
        execute_settlement(user_id, coverage_tier)
```

### Settlement State Machine

- `INGESTED`
- `RISK_SCORED`
- `TRIGGER_VALIDATED`
- `TRUST_EVALUATED`
- `SETTLEMENT_INITIATED`
- `PAYOUT_CONFIRMED`
- `AUDIT_ARCHIVED`

---

## Business Impact

SurakshaPay creates value for both workers and platforms.

| Stakeholder | Value Delivered |
| --- | --- |
| Workers | Immediate financial cushioning, reduced emergency borrowing, transparent rules-based payouts, no claims paperwork |
| Platforms | Better worker trust and retention, reduced support friction during disruptions, auditable emergency support workflows, improved regional risk visibility |
| Insurers / Financial Partners | Event-driven underwriting, stronger fraud resistance, richer telemetry for actuarial modeling, scalable micro-insurance infrastructure |

---

## Tech Stack

### Frontend

- Flutter
- React.js / Next.js
- Tailwind CSS

### Backend

- Node.js
- NestJS
- Python
- FastAPI

### Messaging and Storage

- Apache Kafka or RabbitMQ
- MySQL
- Redis

### Infrastructure

- AWS EC2
- AWS RDS
- AWS S3
- Docker
- GitHub Actions

### Monitoring and Reliability

- Prometheus
- Grafana
- Structured logs
- Alerting and audit queues

---

## Quick Start

### Prerequisites

- Node.js \(v18+\)
- Python \(v3.10+\)
- Docker Engine
- Docker Compose
- MySQL
- Redis
- Kafka or RabbitMQ

### 1. Clone the Repository

```bash
git clone https://github.com/YourOrg/SurakshaPay.git
cd SurakshaPay
```

### 2. Start Infrastructure

```bash
docker compose up -d
```

### 3. Run ML Services

```bash
cd ai-services
python -m venv venv
source venv/bin/activate
# Windows: venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```

### 4. Run Core Backend

```bash
cd ../backend
npm install
npm run start:dev
```

### 5. Run Frontend Dashboard

```bash
cd ../frontend
npm install
npm run dev
```

---

## Security and Reliability

SurakshaPay is designed with production-minded controls.

| Domain | Controls |
| --- | --- |
| Security | JWT or OAuth-based authentication, role-based access control, encrypted secret management, settlement-path request signing, immutable audit logs, data minimization, rate limiting and replay protection |
| Reliability | Retry queues for failed payout requests, idempotent settlement execution, dead-letter handling, cache-backed read optimization, service degradation fallback logic, replayable stream architecture |

---

## Roadmap

- Integration with real insurer or NBFC partners
- Region-wise disruption heatmaps
- Explainable premium dashboard for workers
- Wallet-first and UPI-native payout support
- Offline-first mobile resilience
- Dynamic coverage tiers based on income history
- Reinforcement learning for risk-policy tuning
- Actuarial simulation sandbox for scenario testing

---

## Hackathon Value Proposition

SurakshaPay stands out because it is not just another fintech or insurance app.

It combines:

- **Real social impact**
- **AI + systems engineering**
- **Event-driven architecture**
- **Fraud-aware payout logic**
- **Scalable product thinking**
- **A clear monetization and partnership path**

### Why judges usually like this kind of project

- Solves a real and urgent problem
- Has strong technical depth
- Demonstrates product-market reasoning
- Includes both AI and systems design
- Can scale into an actual startup or B2B platform

---

## Demo Assets

> Replace these placeholders with your actual links before submission.

- **Demo Video:** `https://your-demo-link.com`
- **Pitch Deck:** `https://your-pitch-link.com`
- **Live Prototype:** `https://your-live-app-link.com`
- **Architecture Diagram:** `docs/architecture.png`

---

## Team

**Team Deep Neurals**

### Contributors
- Master AK
- Add team member names here
- Add team member roles here

---

## Disclaimer

This repository is a technical concept and prototype for parametric income protection. Any real-world deployment should use validated actuarial assumptions, verified risk data, regulatory review, partner approvals, and secure financial rails before production use.

---

## Final Pitch

**SurakshaPay transforms income protection from a slow, claim-heavy process into an intelligent, real-time, parametric safety layer for the gig economy.**

When disruption happens, workers should not wait.  
**The system should already know.**

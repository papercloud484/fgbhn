## 🧩 Tech Stack Overview

### 📱 Frontend

| Component | Technologies |
|----------|-------------|
| Mobile App (Rider) | Flutter, Google Maps SDK, Firebase Cloud Messaging |
| Admin Dashboard | React.js (Next.js), Tailwind CSS, Recharts / Chart.js |

---

### 🔐 Backend

| Layer | Technologies / Services |
|------|------------------------|
| Core Backend | Node.js (NestJS) → Core APIs orchestration and business logic |
| AI Services | Python (FastAPI) → AI/ML services |

#### Microservices

| Services |
|----------|
| User Service |
| Policy & Pricing Service |
| Trigger Engine Service |
| Payout Service |
| Fraud Detection |
| Analytics Service |

---

### 🤖 AI/ML Layer

| Component | Technologies |
|----------|-------------|
| Core Stack | Python, Scikit-learn, XGBoost / LightGBM, Pandas, NumPy |

#### Capabilities

| Features |
|----------|
| Risk assessment and scoring |
| Premium calculation with volatility |
| Predictive analytics |
| Adaptive Learning |
| Fraud detection and anomaly detection |

#### 🚀 Model Serving

| Component | Technologies |
|----------|-------------|
| Serving Layer | FastAPI REST endpoints, Dockerized ML services |

---

### 🗄️ Data Layer

| Component | Technologies |
|----------|-------------|
| Primary Database | MySQL |
| Caching & Realtime | Redis |

---

### 🌐 External Integrations

#### Environmental Data

| APIs |
|------|
| OpenWeather API |
| WeatherStack |
| AQI API |

#### Social Disruption Data

| APIs |
|------|
| NewsAPI |
| GNews API |
| Google Maps Platform |
| Mock delivery activity data |
| (Optional) Twitter API |

---

### 📦 Platform Activity Data (Simulated)

| Component | Details |
|----------|--------|
| Mock APIs | Order volume, Rider activity |
| Usage | Detecting demand collapse, Validating real disruption impact |

---

### ⚡ Trigger Engine

| Component | Technologies |
|----------|-------------|
| Engine | Node.js / Python, Apache Kafka / RabbitMQ |

#### Role

| Responsibilities |
|------------------|
| Process real-time data |
| Detect disruption events |
| Trigger payouts |

---

### 💰 Payout System

| Component | Technologies |
|----------|-------------|
| Payments | Razorpay Payout APIs, UPI-based transfers, Webhook-based confirmation |

---

### 🛡️ Fraud Detection

| Component | Technologies |
|----------|-------------|
| Detection Stack | Python ML models, Isolation Forest / LOF, Rule-based validation engine |

---

### 📊 Analytics & Monitoring

| Component | Technologies |
|----------|-------------|
| Dashboard | React Dashboard |
| Monitoring | Prometheus + Grafana |
| Logging | ELK Stack |

---

### ☁️ Cloud & DevOps

| Component | Technologies |
|----------|-------------|
| Cloud | AWS (EC2, S3, RDS - MySQL) |
| Containerization | Docker |
| CI/CD | GitHub Actions |

---

### 🔐 Security

| Component | Technologies |
|----------|-------------|
| Authentication | Firebase Auth / Auth0 |
| Authorization | JWT-based authentication |
| Access Control | Role-Based Access Control (RBAC) |

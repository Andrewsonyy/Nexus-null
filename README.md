# NEXUS NULL++ 🛡️
### AI-Powered Cybersecurity Threat Analysis System

A full-stack web application that analyses real-time telemetry signals to detect and classify cybersecurity threats using machine learning.

---

## 🔍 What It Does

NEXUS NULL++ ingests live telemetry data across multiple system signals and runs it through an ML pipeline to determine threat likelihood, generate investigation questions, and recommend response actions.

**Key capabilities:**
- Real-time telemetry ingestion (login activity, CPU usage, network traffic, file changes, user behaviour)
- ML-based threat classification using scikit-learn (Logistic Regression with fallback model)
- Blind spot detection — flags missing or uncertain signal data
- Dependency analysis — identifies signal correlations indicating threat patterns
- Dynamic investigation question generation based on detected anomalies
- Decision readiness gating — prevents premature threat verdicts on incomplete data
- Interactive dashboard with threat scoring and response recommendations

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Next.js 16, TypeScript, Tailwind CSS, shadcn/ui |
| Backend | Python, FastAPI, Uvicorn |
| ML/Data | scikit-learn, pandas, NetworkX, joblib |
| API | REST, CORS-enabled |

---

## 📁 Project Structure

---

## 🚀 Getting Started

### Backend
```bash
cd backend
pip install -r requirements.txt
uvicorn app:app --reload
```

### Frontend
```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000)

---

## 🧠 How the ML Pipeline Works

1. Telemetry signals are ingested and validated
2. Missing/uncertain values trigger blind spot detection
3. A feature vector is constructed from signal states and threat indicators
4. A trained Logistic Regression model classifies the threat (with a built-in fallback model)
5. Decision readiness is calculated before any verdict is issued
6. Investigation questions are generated dynamically for an analyst to answer
7. Final prediction combines ML output with analyst responses

---

## 👤 Author

**Andrew Sony** — [GitHub](https://github.com/Andrewsonyy) · [LinkedIn](https://linkedin.com/in/andrew-sony)

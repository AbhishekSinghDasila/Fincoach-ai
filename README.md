# FinCoach — AI-Powered Personal Finance Assistant

> Your personal financial advisor, built on your own data.

77% of Indian millennials have no financial plan. They overspend on EMIs,
underinvest, and have zero visibility into their month-end balance.
**FinCoach** analyses your transactions, predicts your financial health,
and lets you ask plain-English questions like _"Can I afford a ₹20,000
phone this month?"_ — answered with real numbers from your own data.

## The Problem

India's personal finance problem is not a lack of money — it is a lack of
visibility and guidance at the right moment. Existing apps like ET Money
or Walnut show charts but do not predict, do not advise, and do not talk
to you. FinCoach fills this gap by combining ML-based cashflow prediction
with a conversational AI layer built on the user's own transaction data.

## What It Does

- **Cashflow prediction** — XGBoost predicts your month-end surplus or deficit
- **Risk scoring** — classifies your financial health as low / medium / high risk
- **Smart categorisation** — ML auto-labels every transaction (food, EMI, rent...)
- **AI chat** — RAG-powered assistant answers questions using your own data
- **Explainability** — every prediction explained via SHAP values

## Tech Stack

| Layer    | Tools                                     |
| -------- | ----------------------------------------- |
| ML       | XGBoost, scikit-learn, SHAP, MLflow       |
| AI       | LangChain, OpenAI / Llama, FAISS          |
| Backend  | FastAPI, PostgreSQL, Redis                |
| Security | JWT auth, rate limiting, input validation |
| DevOps   | Docker, AWS ECS, GitHub Actions CI/CD     |

## Project Structure

```
fincoach-ai/
├── data/               # Raw and processed datasets
├── notebooks/          # EDA and experiment notebooks
├── src/
│   ├── data/           # Data generation and preprocessing
│   ├── models/         # ML model training and evaluation
│   ├── ai/             # LangChain RAG pipeline
│   └── api/            # FastAPI backend
├── models/             # Saved trained models
├── tests/              # Unit and integration tests
└── docker/             # Dockerfile and docker-compose
```

## Business Impact

| Metric       | Value                                            |
| ------------ | ------------------------------------------------ |
| Target users | Indian millennials with no financial plan        |
| Market size  | $1.7B Indian personal finance app market by 2027 |
| Core ML task | Cashflow prediction + risk classification        |
| AI layer     | RAG-powered conversational assistant             |
| Scale        | Designed for 1 lakh concurrent users             |

## Results

_To be updated after model training — Phase 2_

## Setup

### Prerequisites

- Python 3.10+
- PostgreSQL
- Redis
- Docker (for deployment)

### Local Development

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/fincoach-ai.git
cd fincoach-ai

# Create virtual environment
python -m venv venv
source venv/Scripts/activate  # Windows
# source venv/bin/activate    # Mac/Linux

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Edit .env with your actual values

# Run the API
uvicorn src.api.main:app --reload
```

## Development Roadmap

- [x] Phase 1 — Project setup, synthetic data, EDA
- [ ] Phase 2 — ML models: cashflow prediction + risk scoring
- [ ] Phase 3 — RAG-powered AI chat layer
- [ ] Phase 4 — FastAPI backend + PostgreSQL + Redis
- [ ] Phase 5 — Docker + AWS ECS + CI/CD

## Author

**Abhishek Dasila**
Built as a placement project demonstrating end-to-end ML + AI + DevOps skills.

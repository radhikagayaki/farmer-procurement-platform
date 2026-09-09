# Setup Instructions

## Prerequisites

- Node.js 16+ or Python 3.8+
- PostgreSQL 12+
- Redis 6+
- Git

## Backend Setup

### Option 1: Node.js (Express)

```bash
cd backend
npm install
cp .env.example .env
# Edit .env with your configuration
npm run dev
```

### Option 2: Python (FastAPI)

```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env
# Edit .env with your configuration
uvicorn main:app --reload
```

## Frontend Setup

```bash
cd frontend
npm install
npm start
```

The application will be available at `http://localhost:3000`

## Database Setup

```bash
# Create database
psql -U postgres -c "CREATE DATABASE farmer_procurement;"

# Run migrations
# For Node.js:
cd backend && npm run migrate

# For Python:
cd backend && alembic upgrade head
```

## Environment Variables

Create a `.env` file in the backend directory:

```
DATABASE_URL=postgresql://user:password@localhost:5432/farmer_procurement
REDIS_URL=redis://localhost:6379
JWT_SECRET=your_secret_key
SMS_API_KEY=your_sms_api_key
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your_email
SMTP_PASS=your_password
```

## Running Tests

```bash
# Backend tests
cd backend
npm test  # or pytest

# Frontend tests
cd frontend
npm test
```

## Docker Setup

```bash
docker-compose up -d
```

This will start all services (API, database, Redis, etc.)

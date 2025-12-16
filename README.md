# AI Outfit Generator

A cloud-native, AI-powered backend system that analyzes wardrobe images, extracts fashion intelligence, and generates personalized, weather-aware outfit recommendations. This project demonstrates production-level backend engineering using TypeScript, Python, and AWS, with a modular, scalable, and event-driven architecture.

## Overview

This system combines TypeScript for API orchestration, Python for AI/ML processing, and AWS for cloud infrastructure to create an intelligent fashion recommendation platform.

```
┌──────────────────────┐
│  Frontend (Web/App)  │
└──────────┬───────────┘
           │
┌──────────▼─────────────────────┐
│ TypeScript Backend (NestJS)    │
│ Auth · Wardrobe · Outfits      │
│ Analytics · Recommendations    │
└──────────┬─────────────────────┘
           │
┌──────────▼─────────────────────┐
│ Python AI Microservices        │
│ FastAPI · Vision · ML          │
│ Embeddings · Clustering        │
└──────────┬─────────────────────┘
           │
┌──────────▼─────────────────────┐
│ AWS Infrastructure             │
│ S3 · Lambda · RDS · SQS        │
│ EventBridge · CloudWatch       │
└────────────────────────────────┘
```

## Key Features

- Wardrobe image ingestion with AI-powered tagging
- Weather-aware outfit generation based on user preferences
- Embedding-based similarity search and clustering
- Automated daily outfit recommendations
- Travel packing suggestions
- Wardrobe analytics and completeness scoring
- AI stylist chat interface (premium feature)

## Technology Stack

### Backend
- **TypeScript** - NestJS framework for modular backend architecture
- **Python** - FastAPI for AI/ML microservices

### AI and Machine Learning
- Computer vision for image analysis and tagging
- Embeddings and similarity search
- KMeans clustering for outfit combinations
- Color and tone analysis
- LLM-based outfit reasoning

### Cloud Infrastructure (AWS)
- **S3** - Image storage
- **Lambda** - AI inference execution
- **RDS (PostgreSQL)** - Data layer
- **SQS** - Asynchronous job processing
- **EventBridge** - Scheduling and automation
- **CloudWatch** - Logging and monitoring
- **IAM** - Security and permissions management

## Project Structure

```
backend/
  src/
    auth/
    users/
    wardrobe/
    outfit/
    analytics/
    recommendation/
    travel/
    color-analysis/
    premium-stylist/
    commerce/
    jobs/

python-services/
  vision/
  embeddings/
  clustering/
  color-analysis/
```

## Getting Started

### Prerequisites
- Node.js (v16 or higher)
- Python 3.9+
- PostgreSQL
- AWS Account

### Installation

1. Clone the repository:
```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPO.git
cd YOUR-REPO
```

2. Install TypeScript backend dependencies:
```bash
npm install
```

3. Install Python service dependencies:
```bash
pip install -r requirements.txt
```

### Configuration

Create a `.env` file in the root directory with the following variables:

```
DATABASE_URL=postgres://...
JWT_SECRET=your-secret
AWS_ACCESS_KEY_ID=...
AWS_SECRET_ACCESS_KEY=...
AWS_REGION=...
S3_BUCKET_NAME=...
```

### Running the Application

Start the TypeScript backend:
```bash
npm run start:dev
```

Start the Python AI services:
```bash
uvicorn main:app --reload
```

## Architecture Details

### TypeScript Backend (NestJS)
The main API layer handles:
- User authentication and authorization
- Wardrobe management and organization
- Outfit generation orchestration
- Analytics processing
- Background job scheduling

### Python AI Services (FastAPI)
Dedicated microservices for:
- Vision analysis and image processing
- Feature embeddings generation
- Clustering algorithms
- Color analysis and matching
- ML model inference

### AWS Infrastructure
Event-driven, serverless architecture leveraging:
- S3 for scalable image storage
- Lambda for on-demand AI processing
- RDS for reliable data persistence
- SQS for decoupled job processing
- EventBridge for scheduled tasks
- CloudWatch for comprehensive monitoring

## Technical Highlights

This project showcases:
- **Modular Architecture** - Clean separation of concerns with domain-driven design
- **Scalability** - Cloud-native design patterns for horizontal scaling
- **AI Integration** - Production-ready ML pipelines
- **Event-Driven Design** - Asynchronous processing for improved performance
- **Production Quality** - Comprehensive error handling, logging, and monitoring

## Use Cases

- Daily outfit automation based on weather and calendar
- Travel packing list generation
- Wardrobe gap analysis
- Style recommendations
- Outfit history and analytics
- Personal styling assistance

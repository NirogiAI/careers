# Engineering Challenge — Founding Software Engineer
## Overview

This challenge is designed to evaluate your ability to build a real backend system using Python, Linux, and cloud-oriented practices.

This is not an algorithm or puzzle-based test.

We are interested in how you:

structure a system
write production-quality code
handle real-world concerns (errors, logging, performance)
think about deployment and scalability
Objective

Build a small backend service that simulates part of a healthcare workflow system.

The service should:

Accept a patient record
Process the record
Return a structured recommendation

Requirements

## 1. API Service

Build a REST API using Python (FastAPI preferred).

Endpoint 1 — Submit Patient Data

POST /patients

Input (JSON):

{
  "name": "John Doe",
  "age": 45,
  "symptoms": ["chest pain", "fatigue"],
  "history": ["hypertension"]
}

Behavior:

Validate input
Store the record (in-memory or database)
Trigger processing (sync or async)
Endpoint 2 — Get Recommendation

GET /patients/{id}/recommendation

Return:

{
  "patient_id": "123",
  "recommended_specialist": "cardiology",
  "urgency": "high",
  "notes": "Possible cardiovascular issue based on symptoms"
}

## 2. Processing Logic

Implement a simple rule-based system:

Examples:

chest pain → cardiology (high urgency),
headache → neurology,
stomach pain → gastroenterology

You do NOT need real medical accuracy — we are evaluating structure and logic.

## 3. Asynchronous Processing (Important)

Simulate a background processing system:

When patient data is submitted, processing should not block the request
Use one of:
background tasks
Celery
queue system
async workers

## 4. Data Storage

Use one of:

PostgreSQL
SQLite
in-memory (acceptable for MVP)

Structure matters more than scale.

## 5. Logging and Error Handling

Include:

structured logging
clear error responses
basic validation

## 6. Containerization

Provide a Dockerfile that can run the service.

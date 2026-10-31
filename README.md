# Datech

Datech is a full-stack project for freelancers and small service businesses to manage clients, projects, tracked work hours, invoices, and payment-related operations in one place.

## Overview

The application is designed to support everyday freelance workflows, including:
- client and project management
- time tracking and hourly work logs
- invoice creation and status monitoring
- payment tracking
- budget and profitability analysis
- overdue invoice detection
- dashboard alerts for business health indicators

## Stack

- Frontend: React + Vite
- Backend: Java 17 + Spring Boot 3
- Database: PostgreSQL
- API: REST
- Containerization: Docker Compose

## Features

- Client CRUD operations
- Project CRUD operations
- Time entry tracking
- Invoice management
- Payment tracking
- Budget overflow checks by project
- Profitability calculation based on hours and hourly rate
- Overdue invoice detection
- Dashboard alerts endpoint for operational summaries

## Project Structure

```text
.
├── backend/        Spring Boot REST API
├── frontend/       React application
├── docker-compose.yml
├── README.md
└── .gitignore
```

## Run with Docker

From the repository root:

```bash
docker compose up --build
```

This starts:
- PostgreSQL on `localhost:5432`
- backend API on `localhost:8080`

## Run frontend locally

```bash
cd frontend
npm install
npm run dev
```

The frontend runs at `http://localhost:5173` and communicates with the backend at `http://localhost:8080/api`.

## Run backend locally

```bash
cd backend
mvn spring-boot:run
```

## Main API endpoints

- `GET /api/clients`, `POST /api/clients`
- `GET /api/clients/{id}`, `PUT /api/clients/{id}`, `DELETE /api/clients/{id}`
- `GET /api/projects`, `POST /api/projects`
- `GET /api/projects/{id}`, `PUT /api/projects/{id}`, `DELETE /api/projects/{id}`
- `GET /api/projects/{id}/profitability`
- `GET /api/projects/{id}/budget-status`
- `GET /api/time-entries`, `POST /api/time-entries`
- `GET /api/time-entries/{id}`, `PUT /api/time-entries/{id}`, `DELETE /api/time-entries/{id}`
- `GET /api/invoices`, `POST /api/invoices`
- `GET /api/invoices/{id}`, `PUT /api/invoices/{id}`, `DELETE /api/invoices/{id}`
- `GET /api/invoices/overdue`
- `GET /api/payments`, `POST /api/payments`
- `GET /api/payments/{id}`, `PUT /api/payments/{id}`, `DELETE /api/payments/{id}`
- `GET /api/dashboard/alerts`

## Jira / Confluence evidence for HR and project-process review

Project management and process artifacts for this project are available here:

https://drive.google.com/drive/folders/1tMS2l4sFHeHcSxmd6Go3cD8-cN2lq_l-?usp=sharing

This folder includes:
- Jira backlog screenshots and task breakdowns
- workflow examples based on backlog structure and task rules
- Confluence documentation export in PDF format
- supporting project-management evidence demonstrating planning, task tracking, and documentation discipline

This is included to demonstrate practical experience with agile project workflows, backlog management, task ownership, and documentation practices in a real delivery environment.

## Notes

- This is an MVP focused on business workflows and practical domain modeling.
- Authentication and authorization are not implemented yet.
- The project is designed as a solid base for future enhancement, including deployment automation and production hardening.
- Project management process artifacts are kept in a separate evidence folder for review, while the technical implementation remains in this repository.

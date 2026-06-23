# [Log Analyzer](https://github.com/users/butwhole1994/projects/5?pane=info)

Log Analyzer is a backend and infrastructure-focused portfolio project for collecting, processing, searching, and analyzing application logs in a distributed system environment.

The project demonstrates a practical log processing pipeline using Spring Boot, Kafka, OpenSearch, PostgreSQL, Redis, Docker Compose, and AWS-oriented infrastructure design.

## Project Repositories

- [log-analyzer-frontend](https://github.com/butwhole1994/log-anlayzer-frontend)
- [log-analyzer-backend](https://github.com/butwhole1994/log-analyzer-backend)
- [log-analyzer-infra](https://github.com/butwhole1994/log-analyzer-infra)

## Architecture

<img width="4245" height="2343" alt="Image" src="https://github.com/user-attachments/assets/07fa8529-efc4-48e4-b691-ccaa5bb660dd" />

## Log Processing Flow

1. Applications send log events to the Gateway API.
2. The backend validates log events and publishes them to Kafka.
3. Kafka consumers process logs asynchronously.
4. OpenSearch indexes logs for search, filtering, and aggregation.
5. PostgreSQL stores metadata such as projects, services, users, and alert rules.
6. Redis is used for caching and temporary processing status.
7. The frontend provides log search, dashboard, and alert management views.

## Technology Stack

| Category | Technology |
|---|---|
| Frontend | React, Redux Toolkit, TanStack Router |
| Backend | Spring Boot, Spring Cloud Gateway |
| Database | PostgreSQL |
| Search / Log Storage | OpenSearch |
| Cache | Redis |
| Messaging | Kafka |
| CI/CD | GitHub Actions |
| Container | Docker Compose |
| Cloud | AWS |
| CDN / Storage | CloudFront, S3 |

## Technology Decisions

- Kafka is used to decouple log ingestion from log processing and handle logs asynchronously.
- OpenSearch is used for log search, filtering, and aggregation instead of storing searchable logs only in a relational database.
- PostgreSQL is used for relational metadata such as projects, services, users, alert rules, and processing history.
- Redis is used for caching and temporary processing status where persistence is not the primary requirement.
- Docker Compose is used to reproduce the local infrastructure environment consistently.
- AWS is planned as the cloud deployment target after validating the local architecture.

## Core Features

- Log ingestion API
- Kafka-based asynchronous log processing
- OpenSearch-based log indexing and search
- Trace ID-based request tracking
- Dashboard for log statistics and error trends
- Alert rule management
- Local infrastructure with Docker Compose
- AWS deployment planning

## Engineering Focus

This project is not intended to be a simple CRUD application.

The main focus is to demonstrate backend and infrastructure engineering capabilities, including:

- Event-driven architecture
- Asynchronous message processing
- Search indexing and aggregation
- Relational metadata modeling
- Local infrastructure orchestration
- Traceability, retry, DLQ, health checks, and observability
- Cloud deployment design with AWS

## Current Status

This project is currently under active development.

### Implemented

- Repository separation
- High-level architecture design
- Technology stack selection
- Project roadmap and issue management through GitHub Projects

### In Progress

- Local Docker Compose environment
- Backend service skeleton
- Spring Cloud Gateway setup
- Kafka topic design
- PostgreSQL schema design
- OpenSearch indexing strategy

### Planned

- Log ingestion API
- Kafka producer and consumer implementation
- Log search API
- Dashboard UI
- Alert rule management
- GitHub Actions workflow
- AWS deployment documentation

## Getting Started

Setup instructions will be added as the local Docker Compose environment is completed.

Planned local setup:

```bash
# Clone repositories
git clone https://github.com/butwhole1994/log-anlayzer-frontend
git clone https://github.com/butwhole1994/log-analyzer-backend
git clone https://github.com/butwhole1994/log-analyzer-infra

# Start local infrastructure
cd log-analyzer-infra
docker compose up -d
```

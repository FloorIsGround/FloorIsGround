# Hi, I'm Jace

> Software developer with a focus on backend systems, data pipelines, and infrastructure automation.

---
## What I use

- **Languages:** Python, TypeScript, Javascript, Java, C, C++, and C#
- **Databases:** PostgreSQL, Redis
- **Infrastructure:** Proxmox cluster (Primarily work in ubuntu, debian, or mint distros), Cloudflare networking, and I handle my own DNS
- **Tools:** Docker, [pg admin 4](https://www.pgadmin.org/), [Postman](https://www.postman.com/), [Caddy + L4 plugin](https://github.com/mholt/caddy-l4)

---

## Things I do

### Data Engineering
- Applying the ETL pipeline  
- Automated collection of data
- Aggregation and statistics
- Finding useful ways to use that data

**Related Projects:** [LLM Classification](#llm-classification-system), [Large Text Ingestion Service](#document-ingestion-pipeline), [Geospatial Data Pipeline](#live-data-pipeline)

### Backend Development
- API Development and familiarity with many protocols (HTTPS/WSS/gRPC etc.)
- API security and failure point testing
- Optimization of backend software for large scale use
- Database creation, modeling, and management

**Related Projects:** [Geospatial Data Pipeline API](#live-data-pipeline), [Centralized Authentication Service](#centralized-authentication-service), [Invoice & Receipt Service](#invoice--receipt-generation-api-service)


---

## Live Data Pipeline

> Auto-updated stats by a self-hosted runner on my home lab cluster. Data is sourced from a time-series sampling system that has been running continuously since November 2025.

| Metric | Value |
|---|---|
| Total samples collected | 10,801,647 |
| Pipeline running since | November 2025 |
| Days of uptime | 154 |
| Avg samples / day | 70,141 |
| Last recorded sample | 2026-04-28 10:15 UTC |

The pipeline ingests high-frequency samples at a fixed interval, stores them in PostgreSQL, and exposes aggregate metrics here. Collection runs on a self-hosted Proxmox cluster with automated scheduling via GitHub Actions. [Related to this project](#automated-data-collection-and-aggregation-service)

---

## Projects

### Document Ingestion Pipeline
This project on behalf of Fort Hays State University handles automated large text chunking of any book on Project Gutenberg into structured text for the project's purposes for prototyping a new potential literacy program for Northwestern Kansas that leverages personalized learning with AI tutors in early language skills.

**Stack:** Python, PostgreSQL, LangExtract

**Status:** Active

### LLM Classification System
Applies LLMs to automate classification tasks for qualitative research, focused on coding human group impressions through text transcripts, this is primarily under Fort Hays State University's leadership department. Primarily built to use opensource models.

**Stack:** Python, FAISS, RAG, DSPy

**Status:** Active

### Automated Data Collection and Aggregation Service
The above live pipeline statistics are related to this project, which periodically samples location based data and builds a historical database of geospatial coordinate based data for the community it was built for to have more data insights.

**Stack:** Python, PostgreSQL, FastAPI, Uvicorn

**Status:** Active

[Public API](https://dc-gps-data.flooristired.xyz/docs)

### Centralized Authentication Service
As I have made many projects over my time, I decided to centralize my authentication around specific organizations I create them for. To do this I set up my own RBAC scope resolution based auth service, and provide this actively for communities I'm involved with to support software development communities online.

**Stack:** Typescript, PostgreSQL, Vite, React, Zod, Tailwindcss, Fastify

**Status:** Active

[Public Website](https://panoptic-auth-app.flooristired.xyz/)

### Invoice & Receipt Generation API Service
I had a fun idea one day to make a service to generate my own invoices for the purposes of messing around with friends, as well as to serve some small businesses I work with on occasion. So I built a microservice REST API to automate document creation, and generation that should scale well for large use.

I also built this as an embeddable fastify plugin so it could be plugged in easily to any of my other API services if I truly wanted to some day, at this time it runs standalone.

**Stack:** Typescript, PostgreSQL, Redis, Fastify, my own centralized authentication, 

**Status:** Active

The API is not for public use.

---

<sub>Thank you for taking the time to read!</sub>

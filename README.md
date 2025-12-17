# 👋 Hi, I'm Gyowon
Backend Engineer focused on building **AI-integrated web services**  
with an emphasis on reliability, performance, and clear responsibility separation.

I design systems by iterating on limitations discovered in previous projects —  
especially around **latency, scalability, and response reliability**.

I mainly work with **Spring Boot** and **FastAPI**, and I focus on integrating AI components
in a **controlled, performance-aware, and predictable way** rather than relying on fully autonomous AI flows.

![Spring](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=spring&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonaws&logoColor=white)

---

## What I Do
- Design backend systems with clear responsibility boundaries
- Build secure authentication flows using JWT and OAuth2
- Integrate AI models (LLM-based agents) into production-oriented services
- Build real-time interaction servers using WebSocket
- Reduce latency and unnecessary load through caching strategies
- Deploy and manage multi-service environments using Docker and AWS

---

## Tech Stack
- **Backend**: Java (Spring Boot), Python (FastAPI)
- **Security & Auth**: Spring Security, JWT (Access/Refresh), OAuth2 (Kakao)
- **AI Integration**: LLM-based agents (OpenAI API)
- **Database**: MySQL
- **Messaging**: RabbitMQ
- **Caching**: Redis
- **Realtime**: WebSocket
- **Infra**: Docker, Docker Compose, AWS EC2, RDS, S3

---

## How I Think
- I prefer **controlled AI interactions** over fully autonomous flows to ensure service stability
- I design systems assuming **failure cases** such as latency, cache misses, and partial outages
- I value architectural decisions that can be **clearly explained and maintained** by a team

---

## Projects

### 🧓 T-Aging — AI Agent-based Kiosk & Mobile Service
[GitHub Organization](https://github.com/T-Aging)
*(2025.09 – 2025.12)*

- **Role**: Backend / Infrastructure
- **Tech**: Spring Boot, Spring Data JPA, FastAPI, WebSocket, RabbitMQ, MySQL, Redis, Docker, AWS
- **Summary**:  
  Designed the overall system architecture for a real-time kiosk environment,
  including separated local/central databases, session management, AI integration,
  caching strategy, and asynchronous data synchronization.
- **Highlights**:
  - Designed per-user WebSocket sessions to manage conversational state and ordering flow
  - Introduced a two-layer caching strategy with distinct responsibilities:
    - L1 in-memory TTL cache for session-scoped menu snapshots to minimize repeated DB queries
    - L2 Redis cache for FAQ and intent-level responses to reduce redundant LLM calls
  - Applied fuzzy matching for short kiosk queries to improve cache hit rates and reduce response time
  - Evaluated multiple LLM models under latency and availability constraints and selected GPT-4o for real-time usage
  - Defined data ownership boundaries between local (kiosk) and central (mobile) databases
  - Built an event-driven order synchronization pipeline between services using RabbitMQ

---

### 🔍 IM.FACT — Chat-based Climate Fact-checking Service
[GitHub Organization](https://github.com/IM-FACT)
*(2025.03 – 2025.06)*

- **Role**: Backend (AI Pipeline Module)
- **Tech**: FastAPI, OpenAI API, Search APIs
- **Summary**:  
  Improved retrieval quality by introducing LLM-based query rewriting and
  implemented answer composition logic using scraped content.
- **Highlights**:
  - Introduced LLM-based query rewriting and compared retrieval quality between raw queries and rewritten keywords
  - Determined that keyword-based retrieval produced more relevant search results and integrated it into the pipeline
  - Implemented answer generation logic based on scraped content and returned source references with responses
  - Integrated the processing flow with downstream scraping and RAG components

---

### 📘 Bovo — Reading Log Web Service
[GitHub Repository](https://github.com/BookEvolution/bovo_server)
*(2025.01 – 2025.02)*

- **Role**: Backend (Auth / User)
- **Tech**: Spring Boot, Spring Security, JPA (JPQL), MySQL, JWT, OAuth2 (Kakao)
- **Summary**:  
  Implemented authentication and user management features, focusing on JWT-based security and integrating Kakao OAuth2 login.
- **Highlights**:
  - Implemented Access/Refresh token authentication using JJWT and integrated JWT validation into request flows
  - Customized the Spring Security filter chain (added JWT filter, configured CORS) and managed authenticated user context
  - Integrated Kakao OAuth2 login with local JWT issuance for consistent API authentication

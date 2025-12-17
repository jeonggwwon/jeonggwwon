# 👋 Hi, I'm Gyowon

### Backend Engineer building **AI-integrated web services**
with a focus on **reliability, performance, and clear responsibility separation**.

I design systems by iterating on limitations discovered in previous projects —  
especially around **latency**, **scalability**, and **response reliability**.

I mainly work with **Spring Boot** and **FastAPI**,  
and I integrate AI components in a **controlled, performance-aware, and predictable way**  
rather than relying on fully autonomous AI flows.

<p align="left">
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=spring&logoColor=white"/>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonaws&logoColor=white"/>
</p>

---

## 🛠️ What I Do
- 🧩 Design backend systems with **clear responsibility boundaries**
- 🔐 Build secure authentication flows using **JWT & OAuth2**
- 🤖 Integrate **LLM-based AI agents** into production-oriented services
- 🔄 Build real-time interaction servers using **WebSocket**
- ⚡ Reduce latency and unnecessary load through **caching strategies**
- 🚀 Deploy and operate **multi-service environments** using Docker and AWS

---

## 🧰 Tech Stack
- **Backend**: Java (Spring Boot), Python (FastAPI)
- **Security & Auth**: Spring Security, JWT (Access / Refresh), OAuth2 (Kakao)
- **AI Integration**: LLM-based agents (OpenAI API)
- **Database**: MySQL
- **Messaging**: RabbitMQ
- **Caching**: Redis
- **Realtime**: WebSocket
- **Infrastructure**: Docker, Docker Compose, AWS EC2, RDS, S3

---

## 🧠 How I Think
- I prefer **controlled AI interactions** over fully autonomous flows to ensure stability
- I design systems assuming **failure cases** such as latency, cache misses, and partial outages
- I value architectures that are **clearly explainable and maintainable** by a team

---

## 📂 Projects

### 🧓 T-Aging — AI Agent-based Kiosk & Mobile Service
🔗 [GitHub Organization](https://github.com/T-Aging)  
📆 *2025.09 – 2025.12*

**Role**: Backend / Infrastructure  
**Tech**: Spring Boot, Spring Data JPA, FastAPI, WebSocket, RabbitMQ, MySQL, Redis, Docker, AWS

**Summary**  
Designed the overall system architecture for a real-time kiosk environment,  
including separated **local / central databases**, session management, AI integration,  
caching strategies, and asynchronous data synchronization.

**Highlights**
- 🧑‍💻 Designed per-user WebSocket sessions to manage conversational state and ordering flow
- 🗄️ Introduced a **two-layer caching strategy** with distinct responsibilities  
  - **L1**: In-memory TTL cache for session-scoped menu snapshots (DB load reduction)  
  - **L2**: Redis cache for FAQ & intent-level responses (LLM call reduction)
- ⚡ Applied **fuzzy matching** for short kiosk queries to improve cache hit rates and response time
- 📊 Evaluated multiple LLM models under latency & availability constraints and selected **GPT-4o**
- 🔀 Defined data ownership boundaries between local (kiosk) and central (mobile) databases
- 📬 Built an **event-driven order synchronization pipeline** using RabbitMQ

---

### 🔍 IM.FACT — Chat-based Climate Fact-checking Service
🔗 [GitHub Organization](https://github.com/IM-FACT)  
📆 *2025.03 – 2025.06*

**Role**: Backend (AI Pipeline Module)  
**Tech**: FastAPI, OpenAI API, Search APIs

**Summary**  
Improved information retrieval quality by introducing **LLM-based query rewriting**  
and implemented answer composition logic using scraped content.

**Highlights**
- ✏️ Introduced LLM-based query rewriting and compared retrieval quality with raw queries
- 🔎 Determined keyword-based retrieval to be more effective and integrated it into the pipeline
- 🧾 Implemented answer generation logic based on scraped content with source references
- 🔗 Integrated processing flow with downstream scraping and RAG components

---

### 📘 Bovo — Reading Log Web Service
🔗 [GitHub Repository](https://github.com/BookEvolution/bovo_server)  
📆 *2025.01 – 2025.02*

**Role**: Backend (Auth / User)  
**Tech**: Spring Boot, Spring Security, JPA (JPQL), MySQL, JWT, OAuth2 (Kakao)

**Summary**  
Implemented authentication and user management features, focusing on  
JWT-based security and Kakao OAuth2 integration.

**Highlights**
- 🔐 Implemented Access / Refresh token authentication using **JJWT**
- 🛡️ Integrated JWT validation into request flows and managed authenticated user context
- ⚙️ Customized Spring Security filter chains (JWT filter, CORS configuration)
- 🔑 Integrated Kakao OAuth2 login with local JWT issuance for consistent API authentication

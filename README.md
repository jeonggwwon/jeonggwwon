# 👋 Hi, I'm Gyowon

### Backend Engineer building **AI-integrated web services**
with a focus on **reliability, performance, and clear responsibility separation**.

I design systems by iterating on **constraints and trade-offs observed across previous projects** —  
especially around **latency**, **scalability**, and **response reliability**.

I mainly work with **Spring Boot** and **FastAPI**,  
and I integrate AI components in a **controlled, performance-aware, and predictable way**  
rather than relying on fully autonomous AI flows.

I am a Computer Science graduate-to-be, and most of the projects below were built
as team-based academic or capstone projects with production-oriented constraints.

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
- I don’t try to directly fix every limitation I encounter.
  Instead, I pay attention to **where and why certain approaches break down**,
  even in areas outside my immediate responsibility.
- These observations become **decision-making context** in later projects,
  especially when choosing between simpler approaches and more complex ones.
- I believe technical choices should be driven by
  **problem scale, interaction patterns, and operational constraints**,
  not by technology trends alone.
- For AI integration, I prefer designs where behavior is
  **bounded, explainable, and predictable**,
  with clear fallback paths for latency, cache misses, or partial failures.

---

## 📈 Project Growth Timeline

<table>
  <tr>
    <td align="center" width="33%">
      <b>① Bovo</b><br/>
      <sub>2025.01–02</sub><br/><br/>
      <i>Auth / Security</i><br/><br/>
      JWT · OAuth2<br/>
      Spring Security
    </td>
    <td align="center" width="33%">
      <b>② IM.FACT</b><br/>
      <sub>2025.03–06</sub><br/><br/>
      <i>Search & Retrieval Quality</i><br/><br/>
      Query Rewriting<br/>
      Model Evaluation & Docs
    </td>
    <td align="center" width="33%">
      <b>③ T-Aging</b><br/>
      <sub>2025.09–12</sub><br/><br/>
      <i>System Architecture</i><br/><br/>
      WebSocket · Cache · MQ<br/>
      Docker · AWS
    </td>
  </tr>
  <tr>
    <td colspan="3" align="center">
      <sub>Bovo</sub> ─────────▶ <sub>IM.FACT</sub> ─────────▶ <sub>T-Aging</sub>
    </td>
  </tr>
</table>


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
Designed and implemented core modules for **search quality improvement** in an LLM-based fact-checking pipeline,
including **query rewriting, search result evaluation, and answer generation from scraped documents**.

Focused on identifying where retrieval quality degrades in the pipeline
and validating improvements through **model comparison and empirical testing**.

**Highlights**
- 🔍 Implemented a **search module** for document collection and integrated it into the MCP pipeline
- ✏️ Designed an **LLM-based keyword rewriting module** to improve search relevance before retrieval
- 📊 Conducted comparative experiments on:
  - keyword rewriting vs. raw queries
  - different search strategies and models
- 🧾 Built an **answer generation module** that summarizes scraped documents provided by downstream components
- 🧪 Evaluated embedding models, LLM variants, and search configurations to identify trade-offs between quality and latency

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

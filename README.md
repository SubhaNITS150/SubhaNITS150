<h1 align="center">Hi 👋, I'm Subhajyoti Dey</h1>
<h3 align="center">Software Developer | System Design · DevOps · AI/ML</h3>

<p align="center">
  <a href="https://www.linkedin.com/in/subhajyoti-dey-635922235/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:subhajyotidey2910@gmail.com"><img src="https://img.shields.io/badge/Email-Contact-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
  <a href="https://github.com/SubhaNITS150"><img src="https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white" /></a>
</p>

I build **scalable, event-driven, and intelligent systems** — from AI pipelines that turn raw audio into structured data, to multimodal ML models that predict and explain ad performance, to full-stack marketplaces with computer-vision-powered quality control. I care about system design as much as the code itself: how services talk to each other, how failure is isolated, and how a product scales past the demo.

- 🔭 Currently building: **Travenor** (AI travel planning), **MultiModal CTR Predictor**, and a **sustainable commerce platform** (Amazon HackOn)
- 🌱 Currently learning: Deep Learning, MLOps, and Cloud Computing
- 💬 Ask me about: Python, System Design, Machine Learning, JavaScript/TypeScript, Data Structures & Algorithms
- ⚡ Fun fact: I enjoy solving coding challenges and contributing to community projects

---

## 📊 GitHub Stats

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=SubhaNITS150&show_icons=true&theme=radical&count_private=true" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=SubhaNITS150&layout=compact&theme=radical" />
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=SubhaNITS150&theme=radical" alt="GitHub Streak" />
</p>

---

## 🚀 Featured Projects

### 🧳 [Travenor](https://github.com/SubhaNITS150/travenor) — AI-Powered Collaborative Travel Planner

Travenor turns messy, real-world **group meeting audio into structured, actionable travel itineraries**. Instead of one person manually consolidating everyone's preferences after a trip-planning call, Travenor listens, transcribes, extracts intent, and builds the plan automatically — collaboratively, in real time.

**Tech Stack**

| Layer | Technology |
|---|---|
| Frontend | Flutter (real-time state management, mobile-first collaboration) |
| Backend | Node.js, Express.js, Python |
| Database / ORM | PostgreSQL, Supabase, Prisma |
| Messaging | Apache Kafka (event-driven async processing) |
| AI Pipeline | WhisperX (speech-to-text), GLiNER (entity extraction/NLP) |
| DevOps | Docker (local multi-service orchestration) |

**System Design Highlights**
- **Asynchronous by design** — audio ingestion and AI transcription are decoupled from the request/response cycle via Kafka, so the app acknowledges input instantly and processes heavy AI workloads in the background.
- **Component isolation for fault tolerance** — mobile clients, message brokers, and AI services are strictly separated. If the AI pipeline is under load, core trip-planning features stay fully usable.
- **Cloud-native & secure** — built around secure auth, clean API contracts, and real-time sync for multi-user collaboration.

**Workflow**
1. **Input** — users record or upload group meeting audio/transcripts via the Flutter app.
2. **Event publishing** — the backend publishes an event to Kafka and immediately acknowledges the user, without blocking on processing.
3. **AI pipeline** — a consumer service runs the audio through **WhisperX** for transcription, then **GLiNER** extracts entities (locations, dates, preferences, budget constraints).
4. **Itinerary synthesis** — extracted entities are converted into structured, actionable recommendations.
5. **Real-time sync** — the finalized itinerary is persisted to PostgreSQL/Supabase and pushed live to every collaborator's client.

**Why it stands out:** it's a genuine distributed systems problem wrapped around an AI product — Kafka-based decoupling, multi-service orchestration via Docker, and a real NLP pipeline, not just a CRUD app with a chatbot bolted on.

---

### 📈 [MultiModal CTR Predictor](https://github.com/SubhaNITS150/multimodal-ctr-predictor) — Creative Intelligence Engine for Ad Performance

An end-to-end system that predicts **Click-Through Rate (CTR)** for ad creatives by jointly analyzing **image and text**, then goes a step further: it explains *why* an ad performs the way it does and uses that explanation to **generatively suggest better creatives**.

**Tech Stack**

| Layer | Technology |
|---|---|
| Frontend | React (glassmorphism-inspired analytics dashboard) |
| Backend | FastAPI (async, high-performance serving) |
| ML Model | CatBoost Regression (categorical-aware CTR prediction) |
| Interpretability | SHAP (SHapley Additive exPlanations) |
| Generative Layer | LLM-driven creative optimization loop |
| Multimodal Layer | NLP + Computer Vision feature extraction |

**Architecture — Four Layers**
1. **Multimodal Perception Layer** — FastAPI ingests image + text creatives and runs them through NLP/CV pipelines to extract features like color sentiment, text density, emotional tone, and object detection.
2. **Feature Engineering & Data Mapping** — extracted signals are validated and mapped into a strict schema expected by the predictive model.
3. **Predictive Modeling & Attribution** — CatBoost outputs a predicted CTR while SHAP computes per-feature attribution (e.g., *"the blue background increased predicted CTR by 0.5%"*).
4. **Generative Optimization Loop** — SHAP insights are passed to an LLM, which converts them into concrete, natural-language creative recommendations, surfaced directly in the React dashboard.

**Phase 2 Roadmap** *(designed, not yet shipped — demonstrates forward-thinking system design)*
- **Continuous Training Pipeline (MLOps):** Apache Airflow for orchestration + MLflow for model registry + Kafka to stream live ad performance back into scheduled CatBoost retraining.
- **Distributed Feature Store:** Redis / Feast to cache pre-computed features for known assets, keeping FastAPI endpoints fast as feature volume scales into the millions.
- **A/B Testing Simulation Engine:** auto-generate ad variants and score them in parallel through CatBoost to surface the mathematically optimal creative pre-launch.
- **Cross-Platform Transfer Learning:** platform-aware weighting (an image that wins on Instagram may flop on LinkedIn) via platform-specific model routing.

**Why it stands out:** it doesn't stop at "prediction" — it closes the loop from *prediction → explanation → generation*, which is the difference between a model and a product.

---

### 🌱 [Amazon HackOn — Sustainable Commerce Ecosystem](https://github.com/SubhaNITS150/amazon-hackon)

A hackathon-born platform tackling **e-commerce waste at its root**: fraudulent/unnecessary returns, untracked product lifecycles, and inefficient logistics. The system combines **AI-driven return prevention**, digital **"product passports,"** and a **peer-to-peer resale marketplace** into a single sustainable-commerce loop.

**Tech Stack**

| Layer | Technology |
|---|---|
| Frontend | React + Vite, Wouter (routing), Axios |
| Backend | Node.js, Express.js — fully in TypeScript |
| Database / ORM | PostgreSQL (Supabase), Prisma |
| AI/CV Microservice | Python, FastAPI (dedicated damage-detection service, port 8000) |
| Storage & Auth | Cloudinary (image storage), JWT (authentication) |
| Tooling | pnpm workspaces (monorepo management) |

**System Design Highlights**
- **Service isolation** — core marketplace logic (users, listings, transactions) lives in the Express/Prisma backend; AI-based image damage detection is fully decoupled into its own FastAPI microservice.
- **Geospatial-aware logistics** — proximity-based routing (using stored `UserProfile` coordinates) matches buyers/sellers and directs returns to the nearest regional hub, cutting shipping distance and emissions.
- **Strict type safety** — TypeScript + Prisma enforce relational integrity across users, product passports, and marketplace listings, preventing invalid states in a monorepo of this complexity.

**Workflow**
1. **Auth & onboarding** — JWT-based auth, validated environment configuration, seeded admin records, and geospatial profile capture for logistics.
2. **Ingestion & damage detection** — sellers/returners upload item images → images are stored in Cloudinary → the payload is sent to the FastAPI CV microservice, which runs an AI damage-detection model to automatically verify item condition and flag fraudulent returns.
3. **Product passports** — verified items receive an immutable digital record of condition and lifecycle history.
4. **Marketplace & logistics automation** — approved items are auto-listed for P2P resale, with proximity-based routing optimizing regional distribution (e.g., routing through the nearest hub such as Silchar).

**Why it stands out:** it's a full monorepo production system — polyglot microservices (TS + Python), real computer vision in the loop, and a genuine sustainability angle (return-fraud prevention + circular resale) rather than just another marketplace clone.

---

## 🛠️ Skills Snapshot

| Category | Skills |
|---|---|
| **Languages** | Python · JavaScript · TypeScript · SQL |
| **Frontend** | React · Flutter · Vite |
| **Backend** | Node.js · Express.js · FastAPI |
| **Databases & ORM** | PostgreSQL · Supabase · Prisma |
| **Messaging & Streaming** | Apache Kafka |
| **AI / Machine Learning** | CatBoost · SHAP · WhisperX · GLiNER · LLM Integration · NLP · Computer Vision |
| **DevOps & Tooling** | Docker · pnpm workspaces · Git/GitHub |
| **Auth & Storage** | JWT · Cloudinary |
| **Currently Learning (MLOps/Cloud)** | Apache Airflow · MLflow · Redis · Feast · Cloud Computing |

---

## 📫 Connect with Me

<p align="center">
  <a href="https://www.linkedin.com/in/subhajyoti-dey-635922235/"><img src="https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin" /></a>
  <a href="mailto:subhajyotidey2910@gmail.com"><img src="https://img.shields.io/badge/Email-Reach%20Out-red?style=flat&logo=gmail" /></a>
  <a href="https://github.com/SubhaNITS150"><img src="https://img.shields.io/badge/GitHub-Follow-lightgrey?style=flat&logo=github" /></a>
</p>

<p align="center"><i>Thanks for stopping by — always open to collaborating on interesting systems, AI pipelines, and open-source projects!</i></p>

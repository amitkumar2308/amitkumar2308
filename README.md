<div align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=700&size=24&duration=3000&pause=1000&color=70a5fd&center=true&vCenter=true&width=900&lines=Hey+%F0%9F%91%8B+I%27m+Amit+Kumar;AI+%2F+ML+Engineer+%7C+Backend+%26+Systems;LangChain+%7C+RAG+%7C+CNN+%7C+LLMs;Built+Redis+from+Scratch+%E2%80%94+Just+to+Understand+It;2025+B.Tech+Graduate+%7C+Open+to+AI%2FML+%26+SDE+Roles+%F0%9F%9A%80" alt="Typing SVG" />
</div>

<div align="center">
  <a href="https://linkedin.com/in/amitkumar-profile/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  <a href="mailto:amitk.developer23@gmail.com">
    <img src="https://img.shields.io/badge/Email-amitk.developer23@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
  <a href="https://amitkdeveloper.vercel.app" target="_blank">
    <img src="https://img.shields.io/badge/Portfolio-amitkdeveloper.vercel.app-2ea44f?style=for-the-badge&logo=vercel&logoColor=white" />
  </a>
  <a href="https://github.com/amitkumar2308">
    <img src="https://img.shields.io/github/followers/amitkumar2308?label=Followers&style=for-the-badge&color=70a5fd" />
  </a>
</div>

<br/>

---

## 👨‍💻 About Me

I'm an **AI/ML Engineer and Backend Systems Developer** who builds things from scratch — not just to ship, but to understand how they work internally.

I didn't just *use* LLMs — I **built a RAG pipeline with LangChain**, chaining retrieval, embeddings, and LLM calls into a working Q&A system over custom data. I didn't just *use* Redis — I **rebuilt it in C++**, stress-tested it with 10,000 threads, and understood why single-threaded execution is a design choice, not a limitation. That's how I think.

- 🤖 **AI/ML Focus:** LangChain · RAG Pipelines · Custom CNNs · Medical Imaging · LLMs
- ⚙️ **Systems Focus:** Concurrency · Caching · Fault Tolerance · Performance
- 🔬 **Research:** Published paper on ML model behavior (IJSET, Vol. 13, 2025)
- 🏗️ **Approach:** Understand the internals before touching the scale knob
- 🎯 **Goal:** AI/ML Engineer or SDE-1 role — building real, production-grade systems

---

## 🧰 Technical Stack

| **Area** | **Technologies** |
|---|---|
| **Languages** | C++, Python, JavaScript (ES6+), TypeScript, SQL |
| **AI / ML** | TensorFlow, Keras, OpenCV, LangChain, RAG, LLMs, scikit-learn, NumPy, Pandas |
| **Backend** | Node.js, Express.js, Next.js, REST APIs, JWT Auth, Rate Limiting, Microservices |
| **Systems** | Multithreading, Mutex, Condition Variables, Producer–Consumer, Fault Tolerance |
| **Databases** | MongoDB (Indexing, Aggregation), PostgreSQL, MySQL, Redis |
| **Caching** | LRU Eviction, TTL, In-memory KV Stores |
| **Dev Tools** | Git/GitHub, Docker, Linux, AWS (EC2, S3), Vercel, Cloudinary, Postman |
| **Certifications** | IBM AI & Data Science (2025) · Oracle Cloud AI Foundations (2025) |

---

## 🚀 Projects

### 🤖 [LangChain RAG Pipeline](https://github.com/amitkumar2308) — Python · LangChain · LLMs · NLP

> *"Built a full retrieval-augmented generation system — because using ChatGPT is easy, but understanding how to wire your own data into an LLM pipeline is where the real learning is."*

**What I built:**
- Document ingestion pipeline → chunking → embedding model → vector store
- LLM-powered Q&A over custom knowledge bases with context injection
- Prompt engineering for structured, reliable outputs from LLM calls
- Chained LangChain components: loaders → splitters → retrievers → LLM → output parsers

`Python` · `LangChain` · `RAG` · `Embeddings` · `Prompt Engineering` · `LLMs`

---

### 🫁 [Lung Cancer Detection CNN](https://github.com/amitkumar2308/Lung-CancerDetection-CT-Scan-Project-3-) — Python · TensorFlow · OpenCV · Medical AI

> *"Reduced CT scan manual review from 15–20 minutes to under 5 seconds. This is what applied AI looks like."*

**What I built:**
- Complete ML pipeline: data preprocessing with OpenCV + NumPy, class imbalance handling, augmentation
- Custom CNN architecture: design → training → evaluation → deployment
- Binary classification: malignant vs. benign CT scan images
- [Live demo →](https://youtu.be/t4m4qfHG5Yg)

`Python` · `TensorFlow` · `Keras` · `OpenCV` · `NumPy` · `Medical Imaging` · `CNN`

---

### 📸 [PassportPro AI](https://passportphotomaker-psi.vercel.app) — Python · CNN · OpenCV · React · Live on Vercel

**What I built:**
- End-to-end CV app: face detection → background removal → government-spec compliance validation
- Custom CNN classifier checks size, lighting, and face positioning against official standards
- Cuts passport photo prep from 30+ min (studio visit) to under 30 seconds
- Real users, real product — deployed and live

`Python` · `OpenCV` · `CNN` · `React` · `Computer Vision` · `Vercel`

---

### 🔹 [Redis-Lite](https://github.com/amitkumar2308/Redis-Lite) — C++ · Concurrent In-Memory Key-Value Store

> *"Built this to understand why Redis chose single-threaded execution. Turns out it's a deliberate design choice for predictability — not a limitation."*

**Architecture:**
```
Client Threads (N)                Worker Thread (1)
──────────────────                ─────────────────
thread_1 ──┐
thread_2 ──┼──► Command Queue ──► Serial Executor ──► Response
thread_N ──┘    (mutex-locked)    (no data races)     (future/promise)
```

**What I built:**
- Single-worker command queue — all mutations serialized, zero coarse locking
- `SET` / `GET` / `DEL` across N concurrent clients via `std::mutex` + `std::condition_variable`
- TTL-based expiration with `std::chrono::steady_clock` + LRU eviction
- **Stress tested: 10,000 concurrent threads — zero data corruption**

`C++` · `Concurrency` · `Thread Safety` · `LRU` · `TTL` · `System Design`

---

### 🔹 [AnnouncePro](https://github.com/amitkumar2308/AnnouncePro-version-1.0) — Python · Fault-Tolerant Scheduling Daemon

> *Deployed in production at CT University — running across 200+ network-connected endpoints.*

**What I built:**
- Long-running OS-managed background service with persistence across reboots
- Priority-aware, conflict-free job scheduling with ±1s accuracy across 100+ concurrent jobs
- Structured rotating log pipeline + auto-restart failure recovery + Singleton pattern

`Python` · `APScheduler` · `Multithreading` · `Fault Tolerance` · `Structured Logging`

---

### 🔹 [CONNX – Social Platform](https://connx.vercel.app) — Node.js · MongoDB · JWT · Next.js

- 15+ REST API endpoints — JWT auth, social graph, personalised feed
- Compound-indexed MongoDB, rate limiting, pagination, Cloudinary CDN
- Full production deployment — live at connx.vercel.app

`Node.js` · `MongoDB` · `JWT` · `Next.js` · `REST APIs`

---

## 📊 Problem Solving

<div align="center">
  <img src="https://leetcard.jacoblin.cool/amitk2308?theme=tokyonight&font=JetBrains%20Mono&ext=heatmap" alt="LeetCode Stats" />
</div>

<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com?user=amitkumar2308&theme=tokyonight&hide_border=true" width="48%" />
  <img src="https://github-readme-stats.vercel.app/api?username=amitkumar2308&show_icons=true&theme=tokyonight&hide_border=true&rank_icon=github" width="48%" />
</div>

- **300+ problems** solved across Easy, Medium, Hard — top 17% globally
- Focus areas: Trees, Graphs, DP, Sliding Window, Concurrency problems

---

## 💼 Experience

**Backend / Systems Intern — CTech Labs, Ludhiana** *(Dec 2023 – May 2024)*
- Sole feature owner from requirement → production deployment in Agile environment
- Deployed Python scheduling service across 200+ endpoints — reduced manual overhead by ~100%
- Engineered failure recovery, rotating logs, auto-restart; ±1s scheduling accuracy across 100+ jobs

**Full Stack Developer Intern — Suven Consultants (Remote)** *(Jun 2023 – Aug 2023)*
- Built React.js + Node.js client applications; improved page load speed by 20%
- Engineered modular REST APIs integrated with MongoDB in Agile team environment

---

## 🧠 Engineering Philosophy

> *"I prefer understanding how systems work internally — before scaling them externally."*

- **Build to understand** — I've rebuilt Redis in C++ and built my own RAG pipeline from scratch. Using a tool you built teaches you what no docs can.
- **AI that actually works** — not notebooks, but deployed products with real users (PassportPro, Lung Cancer CNN)
- **Correctness before performance** — a fast broken system is worse than a slow correct one

---

## 📬 Let's Connect

Actively looking for **AI/ML Engineer** or **SDE-1 / Backend Engineer** roles.
If you're building in AI, infrastructure, fintech, or distributed systems — let's talk.

<div align="center">
  <a href="mailto:amitk.developer23@gmail.com">
    <img src="https://img.shields.io/badge/Email_Me-amitk.developer23@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white"/>
  </a>
  <a href="https://linkedin.com/in/amitkumar-profile/">
    <img src="https://img.shields.io/badge/LinkedIn-amitkumar--profile-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/>
  </a>
  <a href="https://amitkdeveloper.vercel.app">
    <img src="https://img.shields.io/badge/Portfolio-amitkdeveloper.vercel.app-000000?style=for-the-badge&logo=vercel&logoColor=white"/>
  </a>
</div>

<br/>

<div align="center">
  <img src="https://komarev.com/ghpvc/?username=amitkumar2308&label=Profile+Views&color=70a5fd&style=flat-square" />
  <p><i>AI that works. Systems that scale.</i></p>
</div>

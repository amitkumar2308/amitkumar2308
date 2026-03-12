<div align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=700&size=26&duration=3000&pause=1000&color=70a5fd&center=true&vCenter=true&width=900&lines=Hey+%F0%9F%91%8B+I'm+Amit+Kumar;Backend+Engineer+%7C+Systems+Thinker;C%2B%2B+%7C+Concurrency+%7C+Distributed+Systems;Built+Redis+from+Scratch+%E2%80%94+Just+to+Understand+It;Open+to+SDE+%2F+Backend+Roles+%F0%9F%9A%80" alt="Typing SVG" />
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

I'm a **Backend Engineer** who builds systems from scratch to understand how they actually work under load.

I didn't just *use* Redis — I **built a concurrent in-memory KV store in C++**, stress-tested it with 10,000 simultaneous threads, and analyzed why Redis chose single-threaded execution over per-key locking. That's how I think.

- 🔭 **Current Focus:** Backend systems · Caching · Concurrency · Performance optimization  
- ⚙️ **Mindset:** Think in terms of **latency, throughput, consistency, and fault tolerance**
- 🏗️ **Approach:** Understand the internals before touching the scale knob
- 🤝 **Goal:** SDE / Backend Engineer role on a production engineering team

---

## 🧰 Technical Stack

| **Area** | **Technologies** |
|---|---|
| **Languages** | C++, Python, JavaScript (Node.js), SQL |
| **Backend** | Node.js, Express.js, REST APIs, JWT Auth, Rate Limiting |
| **Systems** | Multithreading, Mutex, Condition Variables, Fault Tolerance |
| **Databases** | PostgreSQL, MongoDB, MySQL |
| **Caching** | Redis, In-memory KV Stores, LRU Eviction, TTL |
| **Concurrency** | Thread Pools, Producer–Consumer, std::promise/future |
| **Scheduling** | APScheduler, Cron Jobs, Background Daemons |
| **Dev Tools** | Git/GitHub, Docker, Linux, Postman, MSYS2/MinGW |
| **Testing** | Stress Testing (10K threads), Load Simulation, Rotating Logs |

---

## 🚀 Projects

### 🔹 [Redis-Lite](https://github.com/amitkumar2308/Redis-Lite) — C++ | Concurrent In-Memory Key-Value Store

> *"Built this because I wanted to understand why Redis uses single-threaded execution. Turns out it's not a limitation — it's a deliberate design choice for predictability and correctness."*

**Architecture:**
```
Client Threads (N)                Worker Thread (1)
──────────────────                ─────────────────
thread_1 ──┐                      
thread_2 ──┼──► Command Queue ──► Serial Executor ──► Response
thread_N ──┘    (mutex-locked)    (no data races)     (future/promise)
```

**What I built:**
- Single-worker command queue — all mutations serialized, **zero coarse locking**
- `SET` / `GET` / `DEL` across N concurrent clients using `std::mutex` + `std::condition_variable`
- Non-blocking `SET`, synchronous `GET` via `std::promise` / `std::future`
- TTL-based expiration using `std::chrono::steady_clock`
- LRU eviction policy for memory management
- **Stress tested: 10,000 concurrent threads — zero data corruption across all runs**

**Key design decision:**  
Analyzed per-key locking vs. command-queue serialization. Chose command-queue for **correctness guarantees and debuggability** — same reason Redis does it.

`C++` · `Concurrency` · `Thread Safety` · `LRU` · `TTL` · `System Design`

---

### 🔹 [AnnouncePro](https://github.com/amitkumar2308/AnnouncePro-version-1.0) — Python | Fault-Tolerant Scheduling Daemon

> *Deployed in production at CT University — running across 200+ network-connected endpoints.*

**What I built:**
- Refactored a UI-driven prototype into a **long-running OS-managed background service** with persistence across reboots
- Time-based, recurring, and priority-aware job scheduling — **conflict-free deterministic execution**
- Structured rotating log pipeline (INFO/DEBUG) — runtime observability without touching UI thread
- Failure recovery: auto-restart policies, deleted-job skip logic, graceful shutdown
- Real-time log streaming to Tkinter UI via 500ms-polling daemon thread
- Singleton pattern to prevent duplicate scheduler instances

**Impact:** Eliminated manual announcement overhead across 200+ campus endpoints.

`Python` · `APScheduler` · `Background Services` · `Fault Tolerance` · `Structured Logging`

---

### 🔹 Campus Reveal — Anonymous Review Platform

**What I built:**
- Backend for anonymous submissions with **abuse-resistant architecture**
- Spam protection via rate limiting (token bucket / fixed window)
- Data integrity guarantees — idempotent write paths
- Focused on **preventing identity leakage** at the storage layer

`Node.js` · `Rate Limiting` · `API Design` · `Data Integrity`

---

## 📊 Problem Solving

<div align="center">
  <img src="https://leetcard.jacoblin.cool/amitk2308?theme=tokyonight&font=JetBrains%20Mono&ext=heatmap" alt="LeetCode Stats" />
</div>

<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com?user=amitkumar2308&theme=tokyonight&hide_border=true" width="48%" />
  <img src="https://github-readme-stats.vercel.app/api?username=amitkumar2308&show_icons=true&theme=tokyonight&hide_border=true&rank_icon=github" width="48%" />
</div>

- **280+ problems** solved across Easy, Medium, Hard
- **Contest Rating: 1500+** — Top 42% globally
- Focus areas: Trees, Graphs, DP, Sliding Window, Concurrency problems

---

## 💼 Experience

**Backend / System Software Engineering Intern — CT University** *(Dec 2023 – May 2024)*

- Sole feature owner from requirement → production deployment
- Designed and deployed campus-wide audio scheduling service (200+ endpoints)
- Engineered failure recovery, structured rotating logs, auto-restart policies
- Reduced silent failures and manual operational overhead significantly

---

## 🧠 Engineering Philosophy

> *"I prefer understanding how systems work internally — before scaling them externally."*

- **Correctness before performance** — a fast broken system is worse than a slow correct one
- **Simple, predictable designs** — complexity is a liability
- **Build from scratch** — using a tool you built yourself teaches you what no docs can

---

## 📬 Let's Connect

I'm actively looking for **SDE-1 / Backend Engineer** roles.  
If you're building something interesting in infrastructure, fintech, or distributed systems — let's talk.

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
  <p><i>Backend first. Systems always.</i></p>
</div>

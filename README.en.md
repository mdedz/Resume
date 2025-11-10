
# 👋 Ilya — Backend & IoT Engineer

[Русский](./README.md)

**Backend & Embedded Engineer** with **5+ years of hands-on experience** in designing and deploying **end-to-end systems** — from low-level device communication (Serial, SAS, ADB) to scalable, containerized backend infrastructures.
I build **production-grade solutions** that integrate IoT devices, real-time telemetry, and modern web platforms — all with a focus on reliability, observability, and maintainability.

---

## 🔭 Summary

I specialize in **IoT and backend engineering**, creating systems that seamlessly connect embedded hardware with robust backend services.
From firmware communication protocols and data pipelines to responsive admin dashboards and CI/CD pipelines — every solution I design is **deployed and running in production** for real clients.

---

## 🎯 Core Technologies

**Python** · Django · FastAPI · Flask · AsyncIO · WebSockets · Docker · Docker Compose · Linux (Debian/Ubuntu) · Nginx · systemd · Bash
**Databases:** MSSQL · PostgreSQL · MySQL · SQLite · Redis
**DevOps & CI/CD:** Git · GitHub Actions · GitLab CI
**Frontend (utility level):** JavaScript · jQuery
**Data & Automation:** Pandas · NumPy · Selenium · cron · ETL pipelines · Data scraping
**IoT & Embedded:** Embedded Linux · Raspberry Pi · Orange Pi · Serial (UART/RS232) · SAS Protocol · ADB · Device telemetry · Secure WebSocket channels · TLS/SSL · JWT · OAuth2
**Rust ecosystem:** Rust · Tokio · Axum · rustls · rcgen
**Other:** Logging · Monitoring · Observability

---

## ⭐ Selected Projects

> *Not all projects in this repository are public — several are proprietary client solutions protected under NDA.*

---

### 1) Metro TV — Centralized Remote Control & Advertising Management for Android TVs

**Overview:**
A production platform for centralized management of Android-based TVs deployed in metro stations. Enables remote control, live telemetry, content updates, and maintenance automation through a single web interface.

**Key features:**

* Full remote control — power relay, source selection, volume, playback, and key emulation.
* Real-time telemetry: power state, connectivity, client health, source, and volume level.
* Encrypted WebSocket channels for secure bidirectional communication.
* Live screen previews and screenshots available on demand.
* Remote maintenance: restart agents, view logs, perform OTA updates, recover faulty clients.
* Visual card editor for creating flexible device control templates.
* Proven scalability — handles 150+ simultaneous remote operations with <1.5 s end-to-end latency; actively managing 47+ devices in production.

**Business impact:**
Eliminated manual servicing trips, cutting operational costs and response times dramatically. Improved uptime of advertising campaigns and service reliability for advertisers.

**[View repository →](https://github.com/mdedz/Metro-TV)**

---

### 2) Casino Clubs Administration System

**Overview:**
Backend infrastructure and device network for collecting, decoding, and visualizing telemetry and transactions from offline slot machines.
Deployed across multiple casino locations, converting raw COM/SAS data into structured financial and operational insights.

**Key features:**

* Real-time COM port data capture and decoding via SAS protocol.
* End-to-end data flow: Agent → WebSocket → Django Server → MSSQL → Admin Panel.
* Live dashboards: transaction logs, wins/losses, player sessions, device analytics.
* Operational utilities: health monitoring, reconciliation reports, event alerts, and historical audit.
* Stable operation in fully isolated (air-gapped) networks.
* 36+ machines in production, <1 s end-to-end response time.

**Business impact:**
Replaced manual, error-prone reconciliation with automated, transparent analytics. Reduced audit time, improved revenue tracking, and enabled instant anomaly detection.

**[Server project →](https://github.com/mdedz/Casino-Administration)**
**[Client agent →](https://github.com/mdedz/SASCollectorService)**

---

### 3) SAS Communication Module

**Overview:**
A robust Python library implementing full **SAS protocol** support for slot machine telemetry and control.

**Features:**

* Complete SAS command support (R, S, M, G).
* Automatic data parsing via `2F` command and persistence to MSSQL.
* Real-time synchronization between internal and external MSSQL instances.
* Flexible listener system (persistent, one-shot, and JSON-configurable command sets).
* Reliable reconnection logic, retries, and exception handling.
* Extendable design — supports custom jackpot and command handlers.

**Stack:** Python · Serial · MSSQL

**[View repository →](https://github.com/mdedz/sas_comm_py)**

---

### 4) Weather Query — Fast, Cached Django Service *(built in 4 days)* ☁️🌃

**Overview:**
A small but production-ready Django application built in just 4 days. Fetches real-time weather data from OpenWeatherMap, caches results, logs queries, and exposes a CI-integrated, Dockerized environment.

**Highlights:**

* Caching with Redis — identical requests within 300 s served from cache.
* Rate limiting per IP with HTTP 429 responses.
* Query history with filters, pagination, and CSV export.
* `/health/` endpoint — monitors DB, Redis, and external API latency.
* Unit-tested critical paths (cache reuse, rate limiting, filtering).
* Full production stack: Docker · docker-compose · Gunicorn · Nginx · GitHub Actions CI.

**Stack:** Python 3.12 · Django 5.2 · PostgreSQL · Redis · Docker · Nginx · Gunicorn · GitHub Actions

**Impact:**
Demonstrates strong backend design principles — caching, observability, and CI/CD — in a minimal yet complete project.

**[View repository →](https://github.com/mdedz/weather_app)**

---

### 5) P2P Chat — Peer-to-Peer Networking Demo (Rust + Tokio + Axum)

**Overview:**
A minimalist, dark-themed peer-to-peer chat and networking framework written in Rust.
Built as a foundation for distributed systems (chat, telemetry, mesh networks) emphasizing security, modularity, and asynchronous design.

**Features:**

* Custom peer-to-peer protocol over TCP with optional TLS (rustls + rcgen).
* Actor-like `PeerManager` for message routing and peer management.
* REST + WebSocket API (Axum): `/peers`, `/send`, `/ws`.
* Static HTML/JS frontend for quick interactive testing.
* Auto-generated self-signed certificates (`--tls`).
* Modular architecture: `server`, `client`, `network`, `protocol`, `web_api`.
* Logging with `tracing` and configurable verbosity (`RUST_LOG`).

**Stack:** Rust · Tokio · Axum · rustls · rcgen · WebSockets

**Purpose:**
Educational and demonstrational project exploring Rust’s async ecosystem — serves as a foundation for future secure P2P or IoT mesh applications.

**[View repository →](https://github.com/mdedz/p2p_rust)**

---
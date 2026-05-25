# 🤖 Personal AI-ChatBOT: Workspace & Context Grounded Interaction Engine

A lightweight, asynchronous full-stack web application built with **FastAPI** and **Python**. The platform integrates secure **Google OAuth 2.0 multi-scope authentication**, handles cryptographic credential token encryption at rest via **Fernet**, extracts real-time user context arrays (Gmail, Google Drive, Calendar), and leverages the **Google Gen AI SDK** to stream grounded responses token-by-token.

---

## 📂 Project Architecture & Directory Structure

The project follows a clean, modular design that strictly separates presentation elements, core backend business logic, configurations, and database interfaces:

```text
AI-ChatBOT/
│
├── static/                  # Client-Side Assets & Interface Styling
│   ├── css/
│   │   └── main.css         # Typography, layout adjustments, and dark themes
│   └── js/
│       └── chat.js          # Asynchronous Event Loops & Fetch Stream Reader
│
├── templates/               # Server-Rendered Jinja2 Templates
│   ├── login.html           # Authorization Gate and Google Action Entry
│   └── chat.html            # Core Conversational Dashboard Workframe
│
├── main.py                  # Core Engine (App Setup, Routing, Middleware Stack)
├── config.py                # Strongly Typed Pydantic Environment Settings
├── workspace_fetcher.py     # Background Worker (Google Discovery API Fetcher)
│
├── .gitignore               # Local Cache, Database, & Credentials Excluder
├── .env.example             # Safe Distribution Environment Template
├── requirements.txt         # Package Software Bill of Materials
└── README.md                # Technical Manual & Operations Guide

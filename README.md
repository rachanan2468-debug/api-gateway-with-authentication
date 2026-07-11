# 🛡️ API Gateway with Authentication

A **secure and scalable API Gateway** built as an interactive, self-contained web application demonstrating system-design fundamentals: JWT-based authentication, RBAC authorization, API routing, rate limiting, load balancing, and request logging — all working in the browser with real crypto.

> **System Design Project** — Centralizes authentication, traffic management, and request routing for a microservices architecture behind a single gateway.

---

## 🚀 Quick Start

```bash
# 1. Install dependencies
npm install

# 2. Start development server
npm run dev

# 3. Open http://localhost:5173
```

That's it — no backend, no database, no config. Everything runs client-side.

### Production build
```bash
npm run build       # outputs to ./dist
npm run preview     # preview the built app locally
```

---

## ✨ Features

| Feature | Implementation |
|---|---|
| 🔑 **JWT Authentication** | Real HMAC-SHA256 signing/verification via Web Crypto API. Tokens include `iss`, `iat`, `exp`, `sub`, `roles` claims. 1-hour expiration. |
| 🛡️ **RBAC Authorization** | Role-based access control (`admin`, `user`) enforced per service route. |
| 🧭 **API Routing** | Path-prefix routing to 5 backend microservices. |
| ⏱️ **Rate Limiting** | **Token-bucket algorithm** — capacity 10, refill 2/sec, per user/IP. |
| ⚖️ **Load Balancing** | Three strategies: **round-robin**, **weighted**, **least-connections**. |
| 📜 **Request Logging** | Every request logged with method, path, status, latency, user, instance, and policy notes. |
| 🌐 **Multiple Backends** | 5 microservices × up to 3 instances each with health status (healthy / degraded / down). |
| 📊 **Live Dashboard** | Real-time traffic charts, KPIs, status distribution, per-service breakdown. |

---
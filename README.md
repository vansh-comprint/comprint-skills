```
   ___                          _       _     ____  _    _ _ _
  / __|___ _ __  _ __ _ _ _ _ _| |_    | |   / ___|| | _(_) | |___
 | |  / _ \ '  \| '_ \ '_| | | ' \|   |  \___ \| |/ / | | / __|
 | |_| (_) | |_| | .__/_| |_|_|_||_|    ___) |   <| | | \__ \
  \___\___/|_|_|_|_|            |____|  |____/|_|\_\_|_|_|___/
```

<p align="center">
  <strong>A growing collection of Claude Code plugins by Comprint.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-1.0.0-blue?style=flat-square" alt="version">
  <img src="https://img.shields.io/badge/plugins-1-brightgreen?style=flat-square" alt="plugins">
  <img src="https://img.shields.io/badge/python-3.12+-yellow?style=flat-square" alt="python">
  <img src="https://img.shields.io/badge/license-MIT-green?style=flat-square" alt="license">
  <img src="https://img.shields.io/badge/claude_code-plugin-8A2BE2?style=flat-square" alt="claude code">
</p>

---

## Quick Start

```bash
# Add the marketplace (one-time)
/plugin marketplace add vansh-comprint/comprint-skills

# Install a plugin
/plugin install comprint-back

# Start using it
/comprint-back scaffold a new FastAPI project with auth
```

That's it. Three commands. You're live.

---

## Plugins

### `comprint-back` — FastAPI Backend Engine

> Your entire FastAPI stack in one command. Architecture, auth, database, testing — all grounded in production patterns.

```
 You                          comprint-back
  │                                │
  │  "add user auth with JWT"      │
  │ ──────────────────────────────>│
  │                                │ ── Classifies: Auth Work
  │                                │ ── Loads: security.md + api-design.md
  │                                │ ── Reads your codebase
  │                                │ ── Designs approach
  │  "Here's what I'll build..."   │
  │ <──────────────────────────────│
  │                                │
  │  "looks good, go"              │
  │ ──────────────────────────────>│
  │                                │ ── Implements using reference patterns
  │                                │ ── Validates: exists? substantive? wired?
  │  JWT + RBAC + endpoints done   │
  │ <──────────────────────────────│
```

#### 9 Knowledge Areas

```
┌─────────────┐ ┌─────────────┐ ┌─────────────┐
│ Architecture │ │  API Design │ │  Database   │
│              │ │              │ │              │
│ 4-layer arch │ │ 5-field resp │ │ Async SQLAl- │
│ Simple+Mod-  │ │ CRUD patter- │ │ chemy, repos │
│ ular layouts │ │ ns, schemas  │ │ Alembic mig- │
│ DI patterns  │ │ Versioning   │ │ rations      │
└─────────────┘ └─────────────┘ └─────────────┘
┌─────────────┐ ┌─────────────┐ ┌─────────────┐
│  Security   │ │   Errors    │ │   Logging   │
│              │ │              │ │              │
│ JWT access+  │ │ Exception   │ │ Structured  │
│ refresh, RBAC│ │ hierarchy,  │ │ JSON, req ID │
│ CORS, rate   │ │ FE-friendly │ │ tracing,    │
│ limiting     │ │ handlers    │ │ ContextVar  │
└─────────────┘ └─────────────┘ └─────────────┘
┌─────────────┐ ┌─────────────┐ ┌─────────────┐
│   Testing   │ │  Background │ │   Common    │
│              │ │    Tasks    │ │   Errors    │
│ Async fixtu- │ │              │ │              │
│ res, FakeRe- │ │ Celery vs   │ │ 10 document-│
│ pository, no │ │ BG Tasks,   │ │ ed preventi-│
│ mocking      │ │ scheduling  │ │ on patterns │
└─────────────┘ └─────────────┘ └─────────────┘
```

#### Smart Routing

The plugin doesn't dump everything into context. It reads your request, picks the right knowledge areas, and loads only what's relevant.

| You say | It loads |
|---------|----------|
| `add authentication` | security + api-design |
| `new project` | architecture + database + logging |
| `fix this 500` | common-errors + exceptions |
| `add background jobs` | background-tasks |
| `something's broken` | investigates first, then decides |

#### Tech Stack

```
FastAPI · Pydantic v2 · SQLAlchemy 2.0 async · PostgreSQL · AsyncPG
Alembic · pytest · httpx · Celery · Redis · JWT · bcrypt
```

#### Example Commands

```bash
/comprint-back scaffold a new FastAPI project with auth and database
/comprint-back add a CRUD endpoint for products with pagination
/comprint-back set up JWT authentication with role-based access control
/comprint-back fix this 422 validation error
/comprint-back add Celery background tasks with Redis
/comprint-back refactor this module to use the repository pattern
```

---

## How It Works

Every plugin in this marketplace follows the same principle: **read before write**.

```
Request ──> Classify ──> Load relevant knowledge ──> Read your codebase
                                                          │
        Done <── Validate <── Implement <── Design ───────┘
                                              │
                                         You approve
```

No generic suggestions. No hallucinated patterns. The plugin reads your existing code, loads curated reference patterns, and adapts to what's already there.

---

## Coming Soon

| Plugin | What it does |
|--------|-------------|
| `comprint-guard` | Real-time architectural guardrails — catches violations on every file write |
| `comprint-scaffold` | Full project generator — Docker, CI/CD, Alembic, logging, health checks in 60 seconds |
| `comprint-api-test` | Auto-generates integration tests from your OpenAPI schema |

---

## Installation

```bash
# Add the marketplace
/plugin marketplace add vansh-comprint/comprint-skills

# Browse available plugins
/plugin list

# Install what you need
/plugin install comprint-back
```

## Contributing

Want to add a plugin to this marketplace? Open a PR with your plugin in `plugins/your-plugin-name/` following the structure of existing plugins.

## License

MIT

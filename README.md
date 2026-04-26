# 🚀 AI Workflow Automation using n8n & LangChain

<div align="center">

![n8n](https://img.shields.io/badge/n8n-Workflow%20Automation-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-AI%20Orchestration-1C3C3C?style=for-the-badge&logo=chainlink&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

An AI-powered workflow automation system built using **n8n** and **LangChain** that enables intelligent automation, data processing pipelines, and seamless integration with external APIs and services.

</div>

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Features](#-features)
- [Tech Stack](#️-tech-stack)
- [Project Structure](#-project-structure)
- [Setup Instructions](#️-setup-instructions)
- [Use Cases](#-use-cases)
- [Project Preview](#-project-preview)
- [Contributing](#-contributing)
- [Author](#️-author)
- [License](#-license)

---

## 🌐 Project Overview

This project demonstrates how to combine **n8n**'s visual workflow automation with **LangChain**'s AI orchestration capabilities to build smart, scalable automation pipelines. Whether you're connecting APIs, processing data, or building intelligent chatbots — this setup gives you a modular foundation to automate it all.

> ⚡ Build once, automate forever.

---

## 🔥 Features

| Feature | Description |
|---|---|
| 🤖 AI-Powered Workflows | Intelligent automation using LangChain agents |
| 🔗 Multi-API Integration | Connect to any REST API or Webhook with ease |
| ⚡ Data Pipelines | Automated end-to-end data processing |
| 🧠 Custom Logic | Extend workflows with JavaScript / TypeScript scripts |
| 🐳 Docker Ready | Pre-configured Docker images for fast deployment |
| 🔒 Security First | Dedicated security configs and policies included |
| 🧪 Fully Tested | Jest + Vitest test setup with coverage reporting |
| 🔄 CI/CD Ready | GitHub Actions workflows pre-configured |

---

## 🛠️ Tech Stack

| Technology | Role |
|---|---|
| [n8n](https://n8n.io/) | Visual workflow automation engine |
| [LangChain](https://www.langchain.com/) | AI agent orchestration & chaining |
| Node.js | Runtime for custom scripts and integrations |
| TypeScript | Typed JavaScript for scalable code |
| Docker | Containerized deployment via `docker/images` |
| pnpm + Turborepo | Monorepo package management & build system |
| Jest / Vitest | Unit and integration testing |
| Biome | Code linting and formatting |

---

## 📂 Project Structure

```
AI-Workflow-Automation-using-n8n-LangChain/
│
├── .agents/                    # AI agent definitions and configs
├── .claude/                    # Claude AI assistant configuration
├── .devcontainer/              # VS Code Dev Container setup
├── .github/                    # GitHub Actions CI/CD workflows
├── .vscode/                    # VS Code workspace settings
│
├── assets/                     # Static assets (images, icons, etc.)
├── docker/
│   └── images/                 # Docker image definitions
├── packages/                   # Monorepo packages
├── patches/                    # Dependency patches
├── scripts/                    # Automation and build scripts
├── security/                   # Security policies and configs
│
├── .env.local.example          # Environment variables template
├── .dockerignore               # Docker build ignore rules
├── .gitignore                  # Git ignore rules
├── biome.jsonc                 # Linter / formatter config
├── jest.config.js              # Jest test configuration
├── package.json                # Root package manifest
├── pnpm-workspace.yaml         # pnpm monorepo workspace config
├── tsconfig.json               # TypeScript configuration
├── turbo.json                  # Turborepo pipeline config
├── vitest.workspace.ts         # Vitest workspace configuration
│
├── AGENTS.md                   # AI agents documentation
├── CHANGELOG.md                # Version history
├── CLAUDE.md                   # Claude-specific instructions
├── CODE_OF_CONDUCT.md          # Community standards
├── CONTRIBUTING.md             # Contribution guidelines
├── SECURITY.md                 # Security policy
├── LICENSE                     # MIT License
└── README.md
```

---

## ⚙️ Setup Instructions

### Prerequisites

- [Node.js](https://nodejs.org/) v18+
- [pnpm](https://pnpm.io/) *(recommended over npm)*
- [Docker](https://www.docker.com/) *(for containerized setup)*

---

### Option A — Run with npx *(Quickest)*

```bash
npx n8n
```

---

### Option B — Run with Docker *(Recommended)*

**Step 1:** Create a persistent volume

```bash
docker volume create n8n_data
```

**Step 2:** Start the n8n container

```bash
docker run -it --rm \
  --name n8n \
  -p 5678:5678 \
  -v n8n_data:/home/node/.n8n \
  docker.n8n.io/n8nio/n8n
```

---

### Option C — Clone & Run Locally

**Step 1:** Clone the repository

```bash
git clone https://github.com/Fasih-Satti/AI-Workflow-Automation-using-n8n-LangChain.git
cd AI-Workflow-Automation-using-n8n-LangChain
```

**Step 2:** Copy environment variables

```bash
cp .env.local.example .env.local
```

**Step 3:** Install dependencies

```bash
pnpm install
```

**Step 4:** Build all packages

```bash
pnpm turbo build
```

---

### Access the Dashboard

```
http://localhost:5678
```

---

## 🎯 Use Cases

| Use Case | Description |
|---|---|
| 🤖 AI Chatbot | Conversational bots powered by LangChain agents |
| 📦 Data Pipelines | Automate data collection, transformation & storage |
| 🔌 API Integrations | Chain multiple APIs into a single smart workflow |
| ✅ Task Automation | Schedule and automate repetitive business tasks |
| 📧 Notifications | Trigger emails, Slack, or webhook alerts on events |

---

## 📸 Project Preview

> 🖼️ *Screenshots and demo GIFs coming soon...*

<!-- Add screenshots below once available:
![Workflow Screenshot](./assets/workflow_preview.png)
![Dashboard](./assets/dashboard.png)
-->

---

## 🤝 Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) and [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) before submitting a pull request.

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a [Pull Request](https://github.com/Fasih-Satti/AI-Workflow-Automation-using-n8n-LangChain/pulls)

> For security-related issues, please refer to [SECURITY.md](SECURITY.md) before opening a public issue.

---

## 🙋‍♂️ Author

**Fasih Ur Rehman**

[![GitHub](https://img.shields.io/badge/GitHub-Fasih--Satti-181717?style=flat-square&logo=github)](https://github.com/Fasih-Satti)

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

<div align="center">
Made with ❤️ by <a href="https://github.com/Fasih-Satti">Fasih Ur Rehman</a>
</div>

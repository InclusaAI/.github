# ![InclusaAI Logo](https://github.com/InclusaAI/.github/raw/main/InclusaAI.png) Welcome to InclusaAI

InclusaAI is building accessible AI solutions that empower everyone. Our platform brings together cutting-edge technology with a commitment to inclusivity and accessibility.

## 🏗️ System Architecture

```
                         ┌───────────────────────────┐
                         │        WEB APPS           │
                         │                           │
                         │ Presenter │ Audience │Admin│
                         └──────────────┬────────────┘
                                        │
                         REST / WS / WebRTC
                                        │
                 ┌──────────────────────┴──────────────────────┐
                 │                                             │
                 ▼                                             ▼
       ┌────────────────────┐                       ┌─────────────────────┐
       │  PLATFORM BACKEND  │                       │ REALTIME MEDIA     │
       │                    │                       │ BACKEND             │
       │ Gateway            │                       │                     │
       │ Identity           │                       │ WebRTC              │
       │ Sessions           │                       │ SFU                 │
       │ Preferences        │                       │ Media ingestion     │
       │ Fanout             │                       │ Signaling           │
       │ Presenter Assist   │                       │ Streaming           │
       └─────────┬──────────┘                       └──────────┬──────────┘
                 │                                             │
                 │ Kafka / gRPC                                 │
                 └───────────────────┬─────────────────────────┘
                                     │
                         ┌───────────▼────────────┐
                         │      AI SERVICES       │
                         │                        │
                         │ ASR                    │
                         │ Sign Recognition       │
                         │ Translation + TTS      │
                         │ Avatar Generation      │
                         │ Vision Quality         │
                         └───────────┬────────────┘
                                     │
                                     ▼
                              AI inference output


       ┌─────────────────────┐              ┌──────────────────────┐
       │ PLATFORM SUPPORT    │              │ INFRASTRUCTURE       │
       │                     │              │                      │
       │ Billing             │              │ Terraform            │
       │ Notifications       │              │ Kubernetes            │
       │ Background Jobs     │              │ Helm                 │
       └─────────────────────┘              │ Monitoring            │
                                            │ CI/CD                 │
                                            └──────────────────────┘


       ┌─────────────────────┐              ┌──────────────────────┐
       │ DESIGN SYSTEM       │              │ DOCUMENTATION        │
       │                     │              │                      │
       │ Components          │              │ Architecture          │
       │ Tokens              │              │ ADRs                  │
       │ Icons               │              │ API                   │
       │ Storybook           │              │ Security              │
       └──────────┬──────────┘              │ Accessibility         │
                  │                         └──────────────────────┘
                  │
                  ▼
          ┌───────────────┐
          │   WEB APPS    │
          └───────────────┘


                 ┌──────────────────────────────┐
                 │      ML RESEARCH             │
                 │                              │
                 │ Experiments                  │
                 │ Dataset research             │
                 │ Model training               │
                 │ Benchmarks                   │
                 └──────────────┬───────────────┘
                                │
                         validated models
                                │
                                ▼
                         ┌───────────────┐
                         │ AI SERVICES   │
                         └───────────────┘
```

## 📦 Repository Organization

Our system is organized into specialized repositories, each serving a critical function:

### Backend Services
- **[backend](https://github.com/InclusaAI/backend)** — Core application backend with business logic, domain services, and API entry points
  - ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
  ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
  ![GraphQL](https://img.shields.io/badge/GraphQL-E10098?style=flat-square&logo=graphql&logoColor=white)

- **[realtime-media-backend](https://github.com/InclusaAI/realtime-media-backend)** — Real-time media plane, architecturally separated from standard business APIs
  - ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
  ![WebRTC](https://img.shields.io/badge/WebRTC-33CC99?style=flat-square&logo=webrtc&logoColor=white)

- **[ai-services](https://github.com/InclusaAI/ai-services)** — AI inference platform powering our ML capabilities
  - ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
  ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
  ![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)

- **[Service-support](https://github.com/InclusaAI/Service-support)** — Supporting platform services
  - ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
  ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)

### Frontend & Applications
- **[web-apps](https://github.com/InclusaAI/web-apps)** — Main frontend monorepo for web applications
  - ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
  ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
  ![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)

- **[mobile-app](https://github.com/InclusaAI/mobile-app)** — Dedicated React Native mobile application
  - ![React Native](https://img.shields.io/badge/React%20Native-61DAFB?style=flat-square&logo=react&logoColor=black)
  ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)

### Platform & Infrastructure
- **[inclusaai-infra](https://github.com/InclusaAI/inclusaai-infra)** — Platform infrastructure and deployment configurations
  - ![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
  ![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
  ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

- **[inclusaai-design-system](https://github.com/InclusaAI/inclusaai-design-system)** — UI/UX design system — single source of truth for design
  - ![Storybook](https://img.shields.io/badge/Storybook-FF6B6B?style=flat-square&logo=storybook&logoColor=white)
  ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)

- **[inclusaai-docs](https://github.com/InclusaAI/inclusaai-docs)** — Engineering knowledge base and documentation
  - ![Markdown](https://img.shields.io/badge/Markdown-000000?style=flat-square&logo=markdown&logoColor=white)
  ![MkDocs](https://img.shields.io/badge/MkDocs-526064?style=flat-square&logo=mkdocs&logoColor=white)

### Research & Development
- **[inclusaai-ml-research](https://github.com/InclusaAI/inclusaai-ml-research)** — ML research and experimentation (intentionally separated from production to maintain code quality boundaries)
  - ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
  ![Jupyter](https://img.shields.io/badge/Jupyter-F37726?style=flat-square&logo=jupyter&logoColor=white)

## 🎯 Our Values

- **Accessibility First** — Building with accessibility as a core feature, not an afterthought
- **Inclusive Design** — Ensuring our products work for everyone
- **Open Collaboration** — We believe great solutions come from diverse perspectives
- **Responsible AI** — Careful, thoughtful development of AI capabilities

## 🚀 Getting Started

Each repository contains its own documentation and setup instructions. Start with the repository most relevant to your interests or contribution area.

## 📚 Documentation

Visit [inclusaai-docs](https://github.com/InclusaAI/inclusaai-docs) for comprehensive engineering documentation, architectural decisions, and contribution guidelines.

## 💬 Questions?

Have questions or ideas? Open an issue in the relevant repository or check our documentation first.

---

*InclusaAI is committed to building AI that works for everyone.*

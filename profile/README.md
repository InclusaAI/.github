# Welcome to InclusaAI

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
- **[realtime-media-backend](https://github.com/InclusaAI/realtime-media-backend)** — Real-time media plane, architecturally separated from standard business APIs
- **[ai-services](https://github.com/InclusaAI/ai-services)** — AI inference platform powering our ML capabilities
- **[Service-support](https://github.com/InclusaAI/Service-support)** — Supporting platform services

### Frontend & Applications
- **[web-apps](https://github.com/InclusaAI/web-apps)** — Main frontend monorepo for web applications
- **[mobile-app](https://github.com/InclusaAI/mobile-app)** — Dedicated React Native mobile application

### Platform & Infrastructure
- **[inclusaai-infra](https://github.com/InclusaAI/inclusaai-infra)** — Platform infrastructure and deployment configurations
- **[inclusaai-design-system](https://github.com/InclusaAI/inclusaai-design-system)** — UI/UX design system — single source of truth for design
- **[inclusaai-docs](https://github.com/InclusaAI/inclusaai-docs)** — Engineering knowledge base and documentation

### Research & Development
- **[inclusaai-ml-research](https://github.com/InclusaAI/inclusaai-ml-research)** — ML research and experimentation (intentionally separated from production to maintain code quality boundaries)

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

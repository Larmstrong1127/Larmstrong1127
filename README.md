<div align="center">

# Landon Armstrong

**LLM Evaluation · Model Fine-Tuning · Full-Stack AI Engineering**

M.S. Computer Science, Saint Martin's University (2024) · Dean's List 2019–2024

[![Portfolio](https://img.shields.io/badge/Portfolio-larmstrong1127.github.io-6366f1?style=for-the-badge&logo=github&logoColor=white)](https://larmstrong1127.github.io)
[![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-DantheMan124-FFD21E?style=for-the-badge)](https://huggingface.co/DantheMan124)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-landon--armstrong-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/landon-armstrong)
[![Email](https://img.shields.io/badge/Email-la.armstrong19@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:la.armstrong19@gmail.com)

</div>

---

## ⚖️ Featured — EvalForge *(LLM evaluation platform + two fine-tuned models)*

> Automates model-vs-model benchmarking: an async FastAPI runner with pluggable provider and judge interfaces, a blind A/B rating room for collecting human preference data, and run-vs-run comparison — behind a Next.js dashboard. CI gates every merge on an eval-regression check.

**I trained and published a preference reward model that beats a public model 2.4× its size.** Bradley-Terry pairwise loss on UltraFeedback, temperature-calibrated, evaluated on a held-out split:

| Model | Params | Pairwise accuracy |
|---|---|---|
| Chance floor | — | 0.5000 |
| `OpenAssistant/reward-model-deberta-v3-large-v2` | 435M | 0.6009 |
| **Mine — `deberta-preference-reward`** | **184M** | **0.7026** |

*Same held-out split (N=1,987), same harness. Honest caveat: in-distribution for my model, out-of-distribution for the public baseline — and mine scores at chance on a small human-preference probe, which is documented on the model card.*

[![Source](https://img.shields.io/badge/Source-Larmstrong1127/evalforge-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Larmstrong1127/evalforge)
[![Reward Model](https://img.shields.io/badge/%F0%9F%A4%97%20Model-deberta--preference--reward-FFD21E?style=for-the-badge)](https://huggingface.co/DantheMan124/deberta-preference-reward)

---

## 🦷 DentaVision *(live in production)*

AI dental treatment planning SaaS, built from firsthand experience as a Patient Care Coordinator. Clinics upload a photo of a printed treatment plan → **Claude Vision** extracts CDT codes, tooth numbers and procedure notes → patients get a prioritized visit schedule on an interactive SVG tooth chart, with an AI chat assistant. Dual-role JWT auth, Stripe subscription billing with webhook sync, 20 Jest tests gating deploys through GitHub Actions.

`React 18` · `Node.js/Express` · `MongoDB Atlas` · `Claude Vision` · `Stripe` · `Vercel + Render`

[![Live Demo](https://img.shields.io/badge/Live%20Demo-denta--vision.vercel.app-34d399?style=for-the-badge&logo=vercel&logoColor=white)](https://denta-vision.vercel.app)
[![Source](https://img.shields.io/badge/Source-Larmstrong1127/DentaVision-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Larmstrong1127/DentaVision)

---

## 🎮 Echoed Nights *(published on Steam)*

My M.S. capstone: a first-person horror game built solo in Unity and C#, taken all the way through commercial release. Enemy AI runs a four-state finite state machine (Patrol → Alert → Chase → Search) over Unity NavMesh, with difficulty that adapts to player performance. I originally architected the AI with reinforcement learning and scoped it down when stable policies proved out of reach on available compute — that decision, and the 19-page capstone report behind it, are in the repo.

[![Steam](https://img.shields.io/badge/Steam-Echoed%20Nights-1b2838?style=for-the-badge&logo=steam&logoColor=white)](https://store.steampowered.com/app/4340810/Echoed_Nights/)
[![Repo](https://img.shields.io/badge/Report%20%26%20Docs-Echoed--Nights--Video--Game-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Larmstrong1127/Echoed-Nights-Video-Game)

---

## ☁️ MedInsight API

Clinical document backend on AWS: containerized FastAPI services on ECS Fargate provisioned with **Terraform** IaC (ECR, S3, DynamoDB), a LangGraph multi-agent pipeline with RAG retrieval, AES-256 encryption and HIPAA-shaped audit logging. Deploys via GitHub Actions using OIDC — no long-lived AWS keys. 40 pytest tests cover auth, encryption and the audit trail end to end.

[![Source](https://img.shields.io/badge/Source-Larmstrong1127/medinsight--api-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Larmstrong1127/medinsight-api)

---

## 🛠 Tech Stack

**Languages** — Python · TypeScript / JavaScript · C# · SQL · R

**ML & AI** — PyTorch · Hugging Face Transformers · Bradley-Terry preference modeling · LLM-as-judge evaluation · RAG · ChromaDB · Ollama (local inference) · Claude / GPT-4 / Gemini APIs

**Web** — FastAPI · Next.js · React · Node.js / Express · ASP.NET Core · Prisma · EF Core

**Data & Infra** — PostgreSQL · MongoDB · SQLite · Redis · Docker · AWS (ECS, ECR, S3, DynamoDB) · Terraform · GitHub Actions CI/CD

---

## 📂 More Projects

| Project | Stack | |
|---|---|---|
| **AgentForge** — multi-LLM agent builder with tool calling and SSE streaming | TypeScript, Next.js 14, Prisma | [→](https://github.com/Larmstrong1127/agentforge) |
| **DocuChat** — RAG document Q&A with cited answers | FastAPI, ChromaDB, Sentence Transformers | [→](https://github.com/Larmstrong1127/DocuChat) |
| **WAVets2Tech** — veteran-to-tech career platform, led a team of 4 | React SPA, ASP.NET Core Web API | [→](https://github.com/Larmstrong1127/WAVets2Tech) |
| **TechCon Convention Site** — exhibitor and booth management | ASP.NET Core MVC, EF Core, SQLite | [→](https://github.com/Larmstrong1127/TechCon-Convention-Site) |
| **A\* Pathfinding** — heuristic search with benchmarks across grid sizes | C# | [→](https://github.com/Larmstrong1127/A-Star-Algorithm) |

---

<div align="center">
<sub>M.S. in Computer Science · building and shipping ML systems · open to AI/ML and full-stack engineering roles · Pacific Northwest</sub>
</div>

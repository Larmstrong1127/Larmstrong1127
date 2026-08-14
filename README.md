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

## 🎞️ Studio tooling — asset-provenance + comfy-workflow-pack

Two halves of one pipeline question: *what made this asset, and how do artists reuse what works?*

**[asset-provenance](https://github.com/Larmstrong1127/asset-provenance)** — a content-addressed registry for AI-generated media: SHA-256 identity, derivation lineage as a DAG, and **OpenUSD export** (provenance in `customData`, lineage as USD relationships). Operated against 1,943 real files from my own generation pipeline: **1,791 assets and 934 derivations registered in 110s** — and the audit found 0 of them had a recoverable model, because generation parameters were never persisted per file. The registry records that as null rather than guessing — and reads embedded **C2PA manifests** (a scan of the same corpus found only 50 of 1,791 carry one). `apr browse` gives artists a thumbnail grid with provenance filters and a clickable lineage graph; `apr demo` takes a reviewer from install to a working lineage view in under two minutes. 134 tests.

**[comfy-workflow-pack](https://github.com/Larmstrong1127/comfy-workflow-pack)** — packages a ComfyUI graph as a versioned workflow pack with a declared, validated artist-safe parameter surface. **Executed end-to-end against ComfyUI 0.32.0**: bound, submitted through its own client, rendered, then registered into the provenance registry and confirmed in a re-opened USD stage. 118 tests; the README states exactly what one run does and does not verify.

## 🦷 DentaVision *(deployed — demo database being restored)*

AI dental treatment planning SaaS, built from firsthand experience as a Patient Care Coordinator. Clinics upload a photo of a printed treatment plan → **Claude Vision** extracts CDT codes, tooth numbers and procedure notes → patients get a prioritized visit schedule on an interactive SVG tooth chart, with an AI chat assistant. Dual-role JWT auth, a Stripe subscription integration (webhook-driven status sync, subscription gating in auth middleware) wired but not processing live payments, and 20 Jest tests gating deploys through GitHub Actions.

`React 18` · `Node.js/Express` · `MongoDB Atlas` · `Claude Vision` · `Stripe` · `Vercel + Render`

[![Live Demo](https://img.shields.io/badge/Live%20Demo-denta--vision.vercel.app-34d399?style=for-the-badge&logo=vercel&logoColor=white)](https://denta-vision.vercel.app)
[![Source](https://img.shields.io/badge/Source-Larmstrong1127/DentaVision-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Larmstrong1127/DentaVision)

---

## 🎮 Echoed Nights *(published on Steam)*

My M.S. capstone: a first-person horror game built solo in Unity and C#, taken all the way through commercial release. Enemy behaviour runs on Unity NavMesh via coroutines and distance thresholds: the monster wanders to random reachable points, chases when you cross a threshold, and — the part I'd defend hardest — backs away when you get too close, because a pursuer you can predict stops being frightening. I originally architected the AI with reinforcement learning and scoped it down when stable policies proved out of reach on available compute. The 19-page capstone report is in the repo; the Unity source is not.

[![Steam](https://img.shields.io/badge/Steam-Echoed%20Nights-1b2838?style=for-the-badge&logo=steam&logoColor=white)](https://store.steampowered.com/app/4340810/Echoed_Nights/)
[![Repo](https://img.shields.io/badge/Report%20%26%20Docs-Echoed--Nights--Video--Game-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Larmstrong1127/Echoed-Nights-Video-Game)

---

## ☁️ MedInsight API

Clinical document backend: a LangGraph ReAct agent with four tools over an encrypted document store, Fernet encryption at rest, and an append-only audit trail. Its AWS footprint (ECS Fargate, ECR, S3, DynamoDB) is **defined in four Terraform modules** and deployed by a GitHub Actions pipeline that authenticates over OIDC — no long-lived keys. To be exact: the infrastructure and pipeline are written but have never been run against a live AWS account; the S3/DynamoDB/KMS paths were exercised against LocalStack instead. 40 pytest tests cover auth, encryption and the audit trail end to end.

[![Source](https://img.shields.io/badge/Source-Larmstrong1127/medinsight--api-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Larmstrong1127/medinsight-api)

---

## 🛠 Tech Stack

**Languages** — Python · TypeScript / JavaScript · C# · SQL · R

**ML & AI** — PyTorch · Hugging Face Transformers · Bradley-Terry preference modeling · LLM-as-judge evaluation · RAG · ChromaDB · Ollama (local inference) · Claude / GPT-4 / Gemini APIs

**Web** — FastAPI · Next.js · React · Node.js / Express · ASP.NET Core · Prisma · EF Core

**Data & Infra** — PostgreSQL · MongoDB · SQLite · Redis · Docker · Terraform · GitHub Actions CI/CD (OIDC) · Vercel · Render · AWS services written in Terraform and run against LocalStack, not a live account

---

## 📂 More Projects

| Project | Stack | |
|---|---|---|
| **AgentForge** — multi-LLM agent builder with tool calling and SSE streaming | TypeScript, Next.js 16, Prisma | [→](https://github.com/Larmstrong1127/agentforge) |
| **DocuChat** — RAG document Q&A with cited answers | FastAPI, ChromaDB, Sentence Transformers | [→](https://github.com/Larmstrong1127/DocuChat) |
| **WAVets2Tech** — veteran-to-tech career platform (university client project) | ASP.NET Core Web API, EF Core | [→](https://github.com/Larmstrong1127/WAVets2Tech) |
| **TechCon Convention Site** — exhibitor and booth management | ASP.NET Core MVC, EF Core, SQLite | [→](https://github.com/Larmstrong1127/TechCon-Convention-Site) |
| **A\* Pathfinding** — heuristic search with benchmarks across grid sizes | C# | [→](https://github.com/Larmstrong1127/A-Star-Algorithm) |

---

<div align="center">
<sub>M.S. in Computer Science · building and shipping ML systems · open to AI/ML and full-stack engineering roles · Pacific Northwest</sub>
</div>

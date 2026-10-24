[한국어](README.md) | English

## Mingeon Park

**I build in-house AI together with the people who use it, then hand it over so they can run and change it themselves.**
I find where AI fits through interviews with staff, build and operate the service, and finish with training and handover.

### In-house AI — QMTech Co., Ltd. (2025.09 – 2026.09, reporting to the CEO)
AI service development and operation, plus in-house AX support (including work for an affiliate). The code is internal, so there are no links.

**1. Safety management ERP** — Java Spring · Next.js · Linux · Docker, on-premises
- Built solo while working out requirements with the safety manager. Kept the existing Excel workflow and automated the repetitive parts
- LLM drafts safety documents. A lightweight model by default; only harder tasks go to a larger model, to control cost
- Personal data passes through a dedicated masking MCP server before reaching the LLM. Admin screens are internal-network only (Tailscale); field inspections use input-only, single-use, time-limited links
- Wrote working rules so the safety manager can modify the system, then handed it over

**2. Industrial safety law RAG chatbot**
- Collects the Serious Accidents Punishment Act, Occupational Safety and Health Act, and Chemicals Control Act via the National Law Information Center Open API, refreshed every 3 days
- Chat Q&A, article summaries, and document drafts grounded in cited articles. Every draft shows the source articles with links to the original text and is confirmed by the manager
- Manager-approved examples are added to the search corpus and used to refine prompts and rules
- Drafting time: 2–3 hours → under 10 minutes (per user feedback)
- Public reconstruction: [constrained-rag](https://github.com/DevMinGeonPark/constrained-rag) — closed-set outputs, deterministic checks, and legal citations on synthetic data

**3. In-house AI training** — about 30 employees of the affiliate
- Two 2-hour sessions (2026.06, 2026.08), then 90-minute one-on-one sessions by appointment: Claude basics, finding automation targets per team, hands-on practice
- Taught asking for sources, setting task-specific instructions, and cross-checking between agents
- One safety staff member went on to manage the site and draft safety documents on their own
- Lab team: reported fewer hallucinations after the training (user feedback, not measured)

### Side project — AIRO (2026.09 –)
**AI travel planning assistant.** Plan a trip in conversation, see it on real road routes, and keep places, booking files, and budget together per trip.
- Trip, itinerary, place, and route tools are defined in one contract (schema and permissions); web chat, the Android app, and MCP clients (Claude, Cursor, etc.) edit the same trip through it
- Supabase Auth with row-level security on every table. MCP calls run with the user's own credentials, so no access to other accounts' trips
- Next.js · TypeScript · Supabase (Postgres) · OpenAI function calling · MCP
- Live: https://airo.dev-heptivision.com · Repository: [DevMinGeonPark/AIRO](https://github.com/DevMinGeonPark/AIRO) (AGPL-3.0)

### Research
| Repository | What | Affiliation · Outcome |
|---|---|---|
| [RoIFuzz](https://github.com/DevMinGeonPark/RoIFuzz) | Fuzzer that mutates ROS 2 IDL messages with SROS 2 security policies enforced | Sejong Univ. ISLab (2024.04–2024.12) · oral presentation, CISC-W'24 (Korea Institute of Information Security & Cryptology) |
| [reinforced-robofuzz](https://github.com/DevMinGeonPark/reinforced-robofuzz) | Earlier stage of RoIFuzz: strengthening RoboFuzz's IDL oracle | Early code of the same study (2024.10) |
| [Grounding-Dino-experiment](https://github.com/DevMinGeonPark/Grounding-Dino-experiment) | Open-set crystal defect detection from text prompts, no training or labels | KITECH Manufacturing AI Research Center, intern (2025.04–2025.06) |
| [EEG2SDiff](https://github.com/DevMinGeonPark/EEG2SDiff) | Encoder that maps EEG to class-separable embeddings (undergraduate thesis) | Oral presentation, KIIS 2023 Spring Conference |
| [Drowsiness-Detection](https://github.com/DevMinGeonPark/Drowsiness-Detection-classification-performance-improvements-resarch) | Data preprocessing for EEG drowsiness detection | Dongseo Univ. ICaN Lab, undergraduate researcher |

**Patent applications (co-inventor)**
- Robot software testing system and method (KR 10-2024-0197496)
- Security vulnerability analysis system for Bluetooth-based smart mobility devices (KR 10-2024-0196091)
- AI-based job experience curation system (KR 10-2023-0171430)

### Teaching
2026.07 guest lecturer (7 hours) — VE·AI program by Hyundai NGV, Samwoo Immersion, and Jeju National University, "Workflow automation with LLMs" for automotive manufacturing staff · Instructor at Coderland (2022.07–2024.05)

### Other public work
- [cs-translation-gpt](https://github.com/DevMinGeonPark/cs-translation-gpt) — Chrome extension that translates multilingual CS inquiries and drafts replies; a data-free rebuild of a tool made during a short-term job
- [agent-eval-harness](https://github.com/DevMinGeonPark/agent-eval-harness) · [rite](https://github.com/DevMinGeonPark/rite) · [gaejo](https://github.com/DevMinGeonPark/gaejo) · [amux](https://github.com/DevMinGeonPark/amux) — personal tools for agent evaluation and managing AI coding work

### Skills
- **Languages** — Python (FastAPI, PyTorch) · Java (Spring) · C · TypeScript (Next.js, React, React Native) · SQL (PostgreSQL)
- **Infra** — Linux · Docker · AWS (Lambda, DynamoDB, CDK) · Supabase
- **AI** — RAG · function calling · MCP · LLM evaluation

### Contact
devmin7985@gmail.com

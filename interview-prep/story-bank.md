# Story Bank — Master STAR+R Stories

This file accumulates your best interview stories over time. Each evaluation (Block F) adds new stories here. Instead of memorizing 100 answers, maintain 5-10 deep stories that you can bend to answer almost any behavioral question.

## How it works

1. Every time `/career-ops oferta` generates Block F (Interview Plan), new STAR+R stories get appended here
2. Before your next interview, review this file — your stories are already organized by theme
3. The "Big Three" questions can be answered with stories from this bank:
   - "Tell me about yourself" → combine 2-3 stories into a narrative
   - "Tell me about your most impactful project" → pick your highest-impact story
   - "Tell me about a conflict you resolved" → find a story with a Reflection

## Stories

<!-- Stories will be added here as you evaluate offers -->
<!-- Format:
### [Theme] Story Title
**Source:** Report #NNN — Company — Role
**S (Situation):** ...
**T (Task):** ...
**A (Action):** ...
**R (Result):** ...
**Reflection:** What I learned / what I'd do differently
**Best for questions about:** [list of question types this story answers]
-->

### [Evaluation & Production] VCHR RAG Pipeline — Eval-Driven Development
**Source:** Reports #002, #003, #004, #005 — Arize AI / LangChain evaluations
**S (Situation):** Virginia Center for Housing Research needed a production RAG system serving real housing policy users across 4 Virginia localities, with zero tolerance for citation errors.
**T (Task):** Build a production RAG pipeline with a rigorous evaluation framework that guaranteed citation accuracy and retrieval quality end-to-end.
**A (Action):** Built with LangChain, Llama 3.3 70B, ChromaDB, self-healing fallback (Together AI primary / Groq secondary), two-pass retrieval with 5-tier geographic/income routing. Created an 86-test automated evaluation framework covering corpus ingestion, retrieval accuracy, and citation grounding. Integrated HUD, BLS, and Census BPS federal APIs with automated startup validation and graceful degradation.
**R (Result):** 6,809 indexed document chunks; citation grounding score of 1.0 across all validation targets; validated across 4 Virginia localities; zero eval failures; system is live and serving real researchers.
**Reflection:** Build evaluation before you optimize — the eval framework found 3 bugs in the retrieval pipeline that would have shipped to production. Evals aren't overhead; they're the forcing function for quality.
**Best for questions about:** production AI deployment, evaluation frameworks, LLMOps, reliability, quality assurance, RAG architecture, working independently, impact measurement

---

### [Adversarial Evaluation & Competition] Amazon Nova Trusted AI — Beat Claude-3.7 Sonnet
**Source:** Reports #002, #003, #004, #005 — Arize AI / LangChain evaluations
**S (Situation):** Amazon Nova Trusted AI Challenge — 6-month multi-tournament safety competition with 10 global teams. Team HokieTokie (Virginia Tech) needed to build the most robust safety-aligned LLM.
**T (Task):** Fine-tune LLMs for adversarial robustness and build an automated evaluation system capable of reproducible regression detection across tournament iterations.
**A (Action):** SFT + DPO on 117K synthetic training examples; built adversarial evaluation system with taxonomy-guided prompt construction and automated quality scoring across vulnerability detection and content filtering categories; optimized inference with model fusion and quantization; deployed dual-expert architecture with sequential filtering.
**R (Result):** 46% adversarial attack success rate reduction; outperformed Claude-3.7 Sonnet and CodeLlama-70B on safety benchmarks; 1st place (Tournament 2) among 10 global teams; 2nd place (Tournament 1).
**Reflection:** The adversarial taxonomy was the core insight — systematic, structured prompting beats random testing by 10x for surfacing vulnerabilities. Automated eval enabled iteration at a pace manual testing couldn't match.
**Best for questions about:** LLM fine-tuning, evaluation systems, adversarial AI, safety, competition performance, outperforming state-of-the-art models, rapid iteration, reproducibility

---

### [Fast Delivery & Multi-Agent] CareRoute — 36-Hour Multi-Agent Deployment
**Source:** Reports #002, #004, #005 — Arize AI / LangChain evaluations
**S (Situation):** Codefest 2025 hackathon — 36-hour deadline, healthcare coordination problem requiring a live deployed system with real autonomous agent coordination.
**T (Task):** Build and deploy a multi-agent healthcare coordination system from scratch in 36 hours, with live deployment to production infrastructure.
**A (Action):** Designed A2A (Agent-to-Agent) protocol for autonomous task delegation across 6 domain-specific microservices using JSON-RPC 2.0; built domain-specific tool invocation with graceful failure recovery; containerized with Docker; deployed to AWS EC2.
**R (Result):** Live multi-agent system deployed in 36 hours; 4th place + Honorable Mention among 60 teams; full A2A protocol working end-to-end.
**Reflection:** Clear inter-agent API contracts beat clever orchestration — simple, explicit protocols scale better than implicit shared state. Under time pressure, scoping ruthlessly (we cut 2 features in hour 8) won us the deployment result.
**Best for questions about:** delivery speed, multi-agent systems, system design under pressure, hackathon experience, AWS deployment, agent orchestration, trade-offs

---

### [Full-Stack Agentic Product] LunaFlow — Shipped Agentic Product to Real Users
**Source:** Reports #004, #005 — LangChain evaluations
**S (Situation):** Personal project to build a real agentic AI assistant — not a demo, but a product with real users and real integrations.
**T (Task):** Design and ship a full-stack agentic product with tool-calling, OAuth 2.0, context management, and automated failure recovery — deployed to real users.
**A (Action):** Built with React/TypeScript/Node.js/FastAPI/PostgreSQL/Docker; LangChain for agent orchestration and tool-calling; integrated Google Calendar, Google Tasks, and ElevenLabs APIs; implemented OAuth 2.0 end-to-end with context management and automated failure recovery.
**R (Result):** Live at lunaflow.work with real users; full tool-calling working across 3 external APIs; end-to-end agentic flows running in production.
**Reflection:** Orchestration is easy in demos, hard in production — context management and failure recovery took longer than the core agent logic. The first real user found 3 bugs in 10 minutes that no test suite anticipated.
**Best for questions about:** full-stack development, agentic systems, product shipping, tool-calling, real users, LangChain, TypeScript, React, entrepreneurial mindset

---

### [Production Observability] AutoUnify ML Scoring Microservice
**Source:** Reports #002, #003, #004 — Arize AI / LangChain evaluations
**S (Situation):** AutoUnify (SF startup, 8-person team) needed real-time visibility into multiple live LLM endpoints integrated into a distributed multi-service architecture.
**T (Task):** Design and deploy a production ML observability microservice that gave the engineering team actionable, real-time signal across their LLM-powered workflows.
**A (Action):** Built with FastAPI, PostgreSQL, Vertex AI; automated CI/CD pipeline with pytest suites and JSON Schema validation across agentic workflows; built reusable prompt engineering components; documented for non-ML team members.
**R (Result):** Real-time observability live across all LLM endpoints; 25% reduction in manual LLM tuning effort; team adopted and used the service.
**Reflection:** In startups, the "quick prototype" always becomes production — build for production from day one. Technical advice only changes behavior if it's actionable — documentation and clarity matter as much as the code.
**Best for questions about:** ML observability, production deployment, startup environment, cross-functional collaboration, LLMOps, microservices, FastAPI

---
name: project-portfolio-roadmap
description: Portfolio project roadmap recommended 2026-06-02 — builds to close gaps for applied roles
metadata: 
  node_type: memory
  type: project
  originSessionId: 0c1ae4fd-0a1a-4f36-a16b-6e7d1156efa7
---

5 projects recommended to maximize candidacy for active applications.

**Why:** Current profile has credential gaps (OSS contributions, Go, SGLang, public fine-tuning work). Projects close specific gaps per role. Amazon Nova win is private — need public equivalents.

**How to apply:** When user asks about projects or what to build next, reference this roadmap. Prioritize by role importance.

## Priority Order

### 1. LangGraph Reference Agent (open-source)
- **Target roles:** LangChain Applied AI (#5), LangChain LangSmith (#4)
- **Score:** 4.3/5
- **Gap it closes:** No open-source contributions; no visible LangChain product familiarity
- **Stack:** LangGraph, Python, evaluation metrics built in
- **Timeline:** 1 week
- **Status:** Not started

### 2. Probe-based Adversarial Intent Detector
- **Target roles:** Anthropic Safeguards (#9), Anthropic Model Evaluations (#10)
- **Score:** 4.8/5 — highest ceiling
- **Gap it closes:** Makes private Amazon Nova adversarial data publicly demonstrable
- **Unique angle:** He has the attack labels — train probes to detect the same attacks from activations
- **Stack:** TransformerLens, sklearn, Llama 3.1 8B, Gradio
- **Metric:** AUROC on held-out adversarial set
- **Timeline:** 1 week
- **Status:** Not started (evaluated as "Option A" in `/career-ops project` mode)

### 3. Public SFT/DPO Fine-tuning Pipeline
- **Target roles:** Anthropic Safeguards (#9), Together AI Research Engineer (#12)
- **Score:** 4.0/5
- **Gap it closes:** Amazon Nova pipeline is closed/private — this makes the capability public and inspectable
- **Note:** Low marginal effort if Nova pipeline code is accessible; reproduce on open-source model
- **Timeline:** 3-5 days
- **Status:** Not started

### 4. Lightweight LLM Eval Harness (pip library)
- **Target roles:** LangChain LangSmith (#4), Anthropic Model Evaluations (#10)
- **Score:** 4.0/5
- **Gap it closes:** VCHR eval framework is internal — abstract it to a reusable library
- **Key positioning:** "mini-LangSmith for RAG pipelines"
- **Timeline:** 1.5 weeks
- **Status:** Not started

### 5. SGLang/vLLM Inference Benchmark + PR
- **Target roles:** Modal FDE (#14)
- **Score:** 3.6/5
- **Gap it closes:** No SGLang contribution explicitly flagged in Modal eval
- **Deliverable:** Blog post + GitHub repo + one PR (even docs)
- **Timeline:** 3-4 days
- **Status:** Not started

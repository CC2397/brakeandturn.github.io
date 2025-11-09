---
title: "Parallel Path Strategy"
layout: default
permalink: /companions/parallel-path-strategy/
---

{% include nav.html %}

# Parallel Path Strategy
*How to brake extractive trajectories and turn toward human–AI symbiosis with working alternatives.*

This guide translates the Compact into **deployable patterns** that communities, co-ops, universities, and municipal partners can run **in parallel** to today’s centralized stacks—reducing dependency while improving reliability, transparency, and stewardship.

🔗 See also: [Living Checklist](living-checklist) · [Companion Index](./) · [Feedback](../feedback)

---

## 1) Strategy at a Glance

**Goal:** Stand up *viable, lawful, open* alternatives beside incumbent AI/infra so people can choose symbiosis now—not after regulation catches up.

**Principles**
- **Local first, federated next.** Keep data + power close to communities.
- **Open by default.** Prefer open weights, open protocols, and auditable ops.
- **Human in the loop.** Humans set intent and approve outcomes.
- **Energy reciprocity.** Compute growth tied to clean energy and local consent.
- **Interoperate; don’t isolate.** Bridge to incumbent systems via open adapters.

---

## 2) Core Patterns (Choose 1–3 to begin)

### P1. Edge + Microgrid Nodes (Civic/University)
- Run small GPU nodes (A100/RTX/MI-series or CPU-optimized LLMs) behind a **microgrid** or **community solar** PPA.
- Offer **local inference** for translation, search, summarization, and routing; burst to cloud only when needed.
- Publish **PUE/WUE + energy mix** monthly.

**Ingredients**
- Hardware: 1–3 modest GPU servers or NUCs
- Stack: Docker + Kubernetes (k3s), Prometheus/Grafana, Ollama/vLLM/TensorRT-LLM
- Data guard: private S3-compatible store (MinIO), VPN, IAM

**Living Checklist tie-ins:** Energy disclosure, human-in-the-loop, model diversity.

---

### P2. Federated Co-op Lab (Healthcare/Education/Legal Clinics)
- Multiple small orgs share **federated training/inference**; data stays local, only model deltas move.
- Uniform **consent + audit** templates; quarterly **alignment stress-tests**.

**Ingredients**
- Fed learning: Flower, FedML, or NVFLARE
- Privacy: DP-SGD configs, secure aggregation, signed deltas
- Governance: Co-op MOU, breach playbook, ethics council minutes (public)

**Living Checklist:** Transparency map, fail-safe, alignment testing.

---

### P3. Open-Policy Procurement Track (City/County/School District)
- Create a standing **symbiosis-first RFP track** that any vendor can meet by adopting the Compact’s **Procurement Rider**.
- Weight awards toward **clean-power disclosures**, **interoperability**, and **open exports**.

**Ingredients**
- Templates: Procurement Rider + Underwriting Addendum (Compact)
- Scoring: [Living Checklist](living-checklist)
- Ledger: Public GitHub/portal with vendor disclosures & contracts

**Living Checklist:** Public ledger, interoperability, community benefit.

---

### P4. Public Knowledge Shield (Libraries/Newsrooms/Universities)
- Maintain a **primary-document archive** and **source verification habit kit** (checklists, browser extensions, classroom modules).
- Publish **model cards** and **dataset cards** for any local AI outputs.

**Ingredients**
- IPFS/Arweave backups; hash-stamped PDFs
- Lightweight fact-check workflows; structured citations
- “First-party only” content policy for public models

**Living Checklist:** Information shield, transparency, cultural alignment.

---

## 3) Phased Rollout

**Phase 0 (0–7 days)**
- Pick 1 pattern + host team.
- Stand up repo/site for disclosures.
- Run the [Living Checklist](living-checklist) baseline.

**Phase 1 (8–30 days)**
- Deploy MVP node(s); publish energy + ops metrics.
- Sign MOUs (utility, campus IT, co-op).
- Start public scorecard with 3–5 KPIs.

**Phase 2 (31–90 days)**
- Add a second site; federate.
- Launch open RFP track; onboard 1 vendor via Rider.
- Publish alignment report + incident playbook.

**Phase 3 (90–180 days)**
- Expand to 3–5 nodes; enable burst-to-cloud with green matching.
- Add workforce reskilling; host a public demo day.
- External audit + checklist re-score.

---

## 4) Governance & Legal Guardrails

- **Human-in-the-Loop Charter:** Define which decisions must be human-approved (domain-specific).
- **Consent & Data Rights:** Clear, revocable terms; deletion on demand; no silent enrichment.
- **Incident Escalation:** 24/48-hour reporting, rollback steps, public post-mortems.
- **Community Benefit:** ≥1% net surplus to local training or energy access.

*All templates released CC0. Use and adapt locally.*  
See: [Feedback](../feedback) to request legal language.

---

## 5) Technical Recipes (copy/paste starting points)

**R1. Local Inference Gateway**
- Ollama/vLLM on k3s; NGINX ingress; JWT auth; per-tenant rate limits.
- Routing: small local model → test → escalate to larger model only on low-confidence.

**R2. Federated Training Sprint**
- Pick a lightweight model (e.g., 1–8B param).
- 3 sites, identical schemas; differential privacy on; signed updates every hour.
- Weekly eval set with human review.

**R3. Energy Telemetry**
- Prometheus node exporter + GPU exporter.
- Grafana dashboard public link: PUE/WUE/energy mix graphs.
- Monthly CSV snapshots in repo.

---

## 6) Quick-Start Kits (deliverables you publish)

- **README + Architecture Diagram** (PNG/SVG)  
- **Ops Runbook** (backup, failover, patch cadence)  
- **Public Metrics** (energy, latency, uptime, incidents)  
- **Model Cards & Dataset Cards**  
- **Checklist Score** (baseline + quarterly)

Place all artifacts in your public repo (or page) for reproducibility.

---

## 7) KPIs (track 3–5 at first)

- % requests served locally vs. cloud burst  
- Energy mix (% renewable) and PUE  
- Median response latency, error rate  
- Human-in-loop approvals per 1k decisions  
- Quarterly **Living Checklist** score (0–5)

---

## 8) Risks & Mitigations

- **Shadow IT / Security drift** → enforce IaC, automated scans, and change logs.  
- **Model overreach** → decision scopes documented; auto-fallback to human.  
- **Cost creep** → local-first routing; burst policies; green credits.  
- **Governance capture** → term limits, public minutes, rotating chairs.  
- **Hype/PR pressure** → publish *working* demos, not promises.

---

## 9) How to Contribute

1. Fork this repo and add a **`/examples/<org>/<pattern>`** folder with your configs.  
2. Open a PR adding your example to the list below.  
3. Or share via the [Feedback](../feedback) page.

**Examples Gallery (add yours)**  
- `examples/city-lib/P1-edge-node/…`  
- `examples/coop-health/P2-fed-lab/…`

---

### License
**CC0 / Public Domain** — copy, adapt, rehost freely.  
Alignment belongs to the commons.

> **Print:** [Download PDF]({{ site.baseurl }}/assets/pdfs/BrakeAndTurn_ParallelPathStrategy_v1.pdf)


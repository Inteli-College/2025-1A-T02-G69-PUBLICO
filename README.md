# Public Report 3 – Mantha Artificial Intelligence

## Sprint 1: Problem Study and Go-to-Market Alignment

**Business Side**

**Week 1** — We consolidated the “Problem Study — Invoice Processing Flow (Logistics),” validating the scenario of **≥ 28,000 invoices/month**, high heterogeneity (NF-e/NFS-e), and irregular image quality. We prioritized risks (tax errors, AP/closing delays, LGPD) and listed root causes using the Ishikawa method (process, systems, document, people, context, and measurement).

**Week 2** — We defined success criteria by **SLA** (lead time per document, accuracy rate, % of exceptions solved on first touch) and tied the commercial narrative to the **Sales Pitch** (value proposition, industry-specific differentiators, and “assisted production” CTA).

**Development Side**

**Week 1** — We mapped the end-to-end technical pipeline: multichannel ingestion, triage, extraction, fiscal/contract validation, and posting; we defined automation checkpoints and **human-in-the-loop** steps.

**Week 2** — We designed the **Authentication and Multi-Tenancy Architecture** (Google Identity Platform + JWT + RLS), with tenant resolution by email and session-based isolation, preparing API contracts and access policies.

## Sprint 2: Internal FinOps and Pricing Engine

**Business Side**

**Week 1** — We published the **cost-reduction pricing model (shared-savings)**, with capture parameters (β), minimum price per task, and auditable baselines by process (logistics and call-center QA).

**Week 2** — We consolidated the **ROI playbook** (baseline vs observed, savings calculation, and scaling ranges) and revenue tables by volume for monitoring — the basis for proposals and pilots.

**Development Side**
**Week 1** — We delivered the **Cost Manager** (LLM + VMs): token-based call logging (input/output/cached), VM costs (E2B), and consolidation by task/project/tenant.
**Week 2** — We finalized the **Cost API** (`GET /companies/cost`) with company-level and run-level aggregations, ensuring adequate latency for consumption dashboards and internal billing audits.

## Sprint 3: Multi-Tenancy & First-Mile Experience

**Business Side**

**Week 1** — We aligned onboarding with prospects (logistics/call center): domain-based invites, profiles (admin/operator/finance), evidence retention (video/logs), and audit responsibilities.

**Week 2** — We defined adoption metrics for **assisted production** (average time per document, exception rate, peak stability).

**Development Side**

**Week 1** — We implemented **Login via GIP**, **JWT** validation in the backend, automatic **tenant resolution**, and **Row Level Security** in the database.

**Week 2** — We published the **consumption screen** on the frontend (credits, cost per tokens and computation, historical chart) with dynamic updates and responsiveness.

## Sprint 4: Execution Transparency (E2B) & Observability

**Business Side**

**Week 1** — We formalized **operational transparency** guidelines: **real-time session link** for the client and **recording retention** for audit purposes.

**Week 2** — We enabled evidence access for stakeholders (videos, structured logs, run statuses) and defined objective acceptance criteria.

**Development Side**

**Week 1** — We integrated **E2B**: **instant VM provisioning**, live link delivery, and **automatic screen recording** (read-only).

**Week 2** — We achieved end-to-end observability: correlation from run → LLM calls → artifacts, metrics (stage time, success/failure, exception rate), and webhooks (start, finish, error).

## Sprint 5: Monitoring Dashboard & Assisted Production

**Business Side**

**Week 1** — We reinforced positioning (technical content on AI automation, differentiators vs traditional RPA) and activated segmented outreach (logistics/call center).

**Week 2** — We structured **assisted production pilots** with proof SLAs (time, quality, exceptions), preparing **shared-savings** contracts with validated baselines.

**Development Side**

**Week 1** — We published the **Monitoring Dashboard** (UX→Front→Back) with KPIs by tenant/project, automation health, run drill-down, and consumption/costs.

**Week 2** — API hardening (versioning, rate limits, retries), **load testing**, and failure simulations (LLM/compute provider degradation). Controlled release to clients under **assisted production**.

## Main Deliverables of the Cycle

* **Problem Study (Logistics)** with bottlenecks, input variability, and risk map.
* **ROI & Pricing Model (shared-savings)** with β and minimum price per task.
* **Cost Manager** (LLM + VM) and **Cost API** with macro and run-level views.
* **Consumption Frontend**: credits, costs, and **historical usage chart**.
* **Authentication & Multi-Tenancy Architecture** (GIP + JWT + RLS).
* **E2B VM Execution**: **live link** and **recording** for audit.
* **Full Observability**: auditable logs, metrics, and events.
* **Updated Sales Pitch** and go-to-market materials for prospecting.

## Next Steps (V3 → V3.1)

1. **Refinement of fiscal extraction** for heterogeneous NFS-e (image preprocessing + consistency validations).
2. **Expansion of connectors** (ERP/TMS/WMS) and posting **safe-guards** with automatic reconciliation.
3. **A/B testing of prompts and model routes** to reduce task cost while maintaining accuracy.
4. **Pilots with shared-savings contracts**, SLAs, and monthly reports with evidence (video + logs + metrics).

**Video Demo of Agent V3**
Available under NDA (includes live E2B session and monitoring dashboard).

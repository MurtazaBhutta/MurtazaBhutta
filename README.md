## Ghulam Murtaza

Senior Generative AI & Forward Deployed Engineer. I take GenAI from a customer's problem to an
auditable production service, and I spend most of my time on the less visible half: evaluation
gates that block a bad release, guardrails and human approval where money or customers are
involved, tenant isolation that holds up under adversarial tests, and the observability that
tells you when a model has quietly got worse.

Currently building multi-agent platforms on LangGraph for 200+ enterprise tenants.

**Portfolio:** [murtazabhutta.github.io](https://murtazabhutta.github.io)

### Work you can inspect

Clean-room rebuilds of patterns I run in production: synthetic data, tests, CI and written design
decisions.

**[django-invoice-agent](https://github.com/MurtazaBhutta/django-invoice-agent)**
*Shows: production Django with an LLM that can't move money on its own.*
Django + DRF + PostgreSQL + Celery. Claude reads supplier invoices from email (structured
outputs); deterministic rules decide whether to post, skip or escalate, with a reason a reviewer
can act on. Each invoice posts exactly once under webhook retries, task redelivery and racing
duplicates, and real-thread PostgreSQL tests check it. An eval gate in CI allows zero unsafe postings.

**[agent-guardrail-runtime](https://github.com/MurtazaBhutta/agent-guardrail-runtime)**
*Shows: per-tenant safety, spend control and data isolation for agents.*
Seven composable layers around an agent's model call: kill switch, guardrails, human approval,
cost cap, step recorder, tracing and retries. Tenant isolation is enforced by PostgreSQL
row-level security, and CI fails if the isolation tests are skipped.

**[llm-release-gate](https://github.com/MurtazaBhutta/llm-release-gate)**
*Shows: no model version ships without passing regression evals.*
A regression eval harness wired into CI as a required check. Hard safety failures are checked
against absolute floors, so committing a worse baseline cannot launder them, and a self-test
fails if the gate ever stops gating.

### Focus

Agentic AI and LangGraph multi-agent orchestration · RAG (vector and graph) · LLM evaluation and
LLMOps · guardrails and human-in-the-loop · forward-deployed delivery, PoC to production ·
Python, Django, FastAPI, PostgreSQL

---

📍 Lahore, Pakistan · open to remote (US/UK hours) and relocation ·
[LinkedIn](https://linkedin.com/in/ghulam-murtaza-9024071a5)

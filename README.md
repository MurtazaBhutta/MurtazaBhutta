## Ghulam Murtaza

Senior AI / GenAI Engineer. I build production multi-agent LLM systems — and mostly the
unglamorous half: evaluation gates that block a bad release, tenant isolation that holds
under adversarial tests, guardrail middleware, and the observability that tells you when a
model has quietly got worse.

Currently building agent platforms serving 200+ enterprise tenants.

### Work you can inspect

**[llm-release-gate](https://github.com/MurtazaBhutta/llm-release-gate)**
*Proves: no model version ships without passing regression evals.*
A regression eval harness wired into CI as a required check. Assertions are scored in
tiers; hard safety failures are checked against absolute floors, so committing a worse
baseline cannot launder them. A third CI job feeds the gate a known-bad run and fails if
it passes — guarding the real failure mode, which is a gate decaying into a no-op that
reports green forever.

More repos are in progress. They get listed here when they are finished and tested, not
when they are started.

### Focus

LangGraph and multi-agent orchestration · RAG, vector and graph-backed · LLM evaluation
and LLMOps · guardrail and HITL middleware · PostgreSQL row-level security · Python

---

📍 Lahore, Pakistan · [LinkedIn](https://linkedin.com/in/ghulam-murtaza-9024071a5)

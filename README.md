# RegulaFlow
 Autonomous AI Compliance and Risk Monitoring Agent.
 An autonomous AI agent that continuously monitors documents, policies, and AI system changes, then detects compliance risks, explains them, and proposes corrective actions without human prompting.
 RegulaFlow operates as a long-running background agent. It reasons over changes as they occur, records auditable decisions, and exposes its internal state through a passive observability dashboard.

# Autonomous Agent Design
 1. RegulaFlow runs as a continuous loop:
 2. Loads prior agent state and memory
 3. Detects new system or policy changes
 4. Reasons over regulatory impact using Gemini 3
 5. Determines whether a compliance risk exists
 6. Assigns severity and justification
 7. Proposes mitigation steps (when applicable)
 8. Persists decisions for auditability
 9. Sleeps and repeats
<Br>No user prompts are required for operation.


### Flow:

1. **Observe**
   - Detect new system changes (feature updates, data usage changes, etc.)

2. **Reason**
   - Analyze changes against regulatory policies (e.g., GDPR, AI Act)

3. **Decide**
   - Determine if a compliance risk exists
   - Assign severity + explanation

4. **Store**
   - Save decision as an auditable record

5. **Repeat**
   - Runs continuously without human input

---

## 🧩 System Architecture
[ System Changes ] <br>
↓ <br>
[ Agent Loop (FastAPI Worker) ] <br>
↓ <br>
[ AI Reasoning Engine (LLM / Gradient AI) ] <br>
↓ <br>
[ MongoDB (State + Audit Logs) ] <br>
↓ <br>
[ HTMX Dashboard (Observability UI) ] <br>

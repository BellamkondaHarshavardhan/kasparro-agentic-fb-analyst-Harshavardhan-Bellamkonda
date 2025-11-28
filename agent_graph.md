# Agentic Workflow (Planner → Evaluator → Generator)

User Query → "Analyze ROAS drop and suggest creatives"

┌─────────────┐
│   Planner   │ → Breaks query into subtasks
└──────┬──────┘   1. Load & summarize data
       │         2. Generate hypotheses
       │         3. Validate quantitatively
       │         4. Generate new creatives
       │         5. Write final report
       ↓
┌─────────────┐    ┌──────────────┐    ┌────────────────┐
│ Data Agent  │───▶│ Insight Agent│───▶│ Evaluator Agent│ → Rejects hallucinations
└─────────────┘    └──────────────┘    └───────┬────────┘   (confidence <0.9 → retry)
                                                   ↓
                                       ┌─────────────────────┐
                                       │ Creative Generator  │ → 12 new ideas grounded in winners
                                       └─────────────────────┘
                                                   ↓
                                       ┌─────────────────────┐
                                       │   Report Writer     │ → report.md
                                       └─────────────────────┘

Evaluator loop ensures every number in insights.json matches the actual CSV.

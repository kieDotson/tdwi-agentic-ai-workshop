# Lab 4 — The Inherited Agent

In this capstone lab, you inherit an undocumented reconciliation agent and decide whether it can be trusted.

The agent appears to work, but its standard Q3 run reports **$4.0M** by averaging the Finance and Sales figures rather than reconciling the $400K discrepancy.

The lab moves through five operating stages:

**See it → Measure it → Break it → Encode it → Monitor it**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kieDotson/tdwi-agentic-ai-workshop/blob/main/lab-4-production-reliability/lab-4-production-reliability.ipynb)

## Start Here

1. Open the notebook in Colab.
2. Run the setup cells from top to bottom.
3. Enter the temporary workshop Gemini API key when prompted.
4. Launch Phoenix and keep the Phoenix interface available while you work.
5. Run the standard case and inspect its trace.
6. Run the pre-built golden set.
7. Red-team the inherited system with at least two adversarial probes.
8. Turn one reproduced failure into a new evaluation case.
9. Add the required guardrail and re-run the suite.
10. Finish with the monitoring-threshold exercise.

## What You Will Use

- **Arize Phoenix** for AI observability and trace inspection
- **OpenTelemetry** as the underlying tracing standard
- **OpenInference** for AI-specific instrumentation semantics
- **Python deterministic evaluators** for the golden set
- **A manual probe harness** for red teaming
- **Plain Python guardrails** for production controls

## Why the Red Teaming Is Manual

The workshop intentionally does not automate the attack exercise with a red-team framework.

Your job is to decide how you would try to break the system, reproduce the defect, and identify where it becomes visible in the trace.

Production tools can automate attack generation later. The methodology comes first.

## Required Attendee Work

You will:

- diagnose the inherited averaging failure from a trace;
- interpret a six-case evaluation baseline;
- design at least two adversarial probes;
- add one of your own reproduced failures to the golden set;
- choose the residual escalation threshold;
- re-run the suite after hardening; and
- define one production monitoring signal and alert threshold.

## Files

Recommended repo structure:

```text
lab-4-production-reliability/
├── README.md
├── lab-4-production-reliability.ipynb
└── lab4_agentops_workflow.png
```

The notebook embeds the workflow diagram directly, and the standalone PNG is included for reuse in workshop materials.

## Saving Your Work

Opening the notebook from GitHub does not modify the workshop repository.

Use **File → Save a copy in Drive** in Colab if you want to keep your own edited version.

# Lab 3 — The Reconciliation Crew

In this lab, you will expand the Morrow Peak Outfitters reconciliation system from a single controlled agent into a manager-plus-specialists architecture.

The Lab 2 agent stopped correctly with **$180,000 explained** and **$220,000 unresolved**. Lab 3 gives the system the additional evidence and specialization it needs to close the full **$400,000** discrepancy.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kieDotson/tdwi-agentic-ai-workshop/blob/main/lab-3-reconciliation-crew/lab-3-reconciliation-crew.ipynb)

## Start Here

Click **Open in Colab** above.

Then:

1. Run the notebook from top to bottom.
2. Enter the temporary workshop Gemini API key when prompted.
3. Read the Markdown explanations before each code section.
4. Complete the **YOUR TURN** and engineering checkpoint sections.
5. Compare the crew's behavior before and after the reconciliation skill file is introduced.
6. Verify that the final residual closes to zero and that all cited evidence can be checked.

Most of the Python is already written. The goal is to make architecture, orchestration, retrieval strategy, state, and methodology visible.

## What You Will Build

You will work with a LangGraph-based reconciliation crew made up of:

- **Manager Agent** — tracks the residual and decides which specialist should work next
- **Warehouse Analyst** — uses structured SQL over Finance and Sales data
- **Documentation Researcher** — searches metric definitions and data documentation
- **Change Historian** — searches tickets and dbt change history
- **Residual Ledger** — deterministically tracks how much of the discrepancy remains unexplained
- **Reconciliation Skill File** — makes the investigation methodology explicit

## Architecture

The notebook includes the Lab 3 architecture diagram directly in the notebook.

The standalone image is also included in this folder as:

`lab3_architecture_diagram.png`


## Skill Artifact

`reconciliation-skill.md` is a real Markdown artifact that contains MPO's reconciliation methodology.

The notebook loads the file, asks you to complete two decision points, and writes a completed runtime copy. The skill contains process knowledge—sequence, checks, completion criteria, and escalation rules—while the workers and tools provide the capabilities used to execute that process.

## Lab Pass Condition

The lab is complete when the system identifies all three supported causes:

| Cause | Amount |
|---|---:|
| Refund recognition timing | $180,000 |
| Net revenue definition mismatch | $150,000 |
| Undocumented dbt model change | $70,000 |
| **Total** | **$400,000** |

The final residual should be **$0**, and every cited ticket, document, or refund identifier should be verifiable in the source data.

## Files

Recommended repo structure:

```text
lab-3-reconciliation-crew/
├── README.md
├── lab-3-reconciliation-crew.ipynb
├── reconciliation-skill.md
└── lab3_architecture_diagram.png
```

The current notebook creates its small workshop fixtures in code so attendees can run the lab without separately uploading source files.

## What to Pay Attention To

As you work through the notebook, focus on:

- why the problem now justifies multiple specialists;
- how evidence type influences retrieval method;
- what belongs in the manager versus the workers;
- how context is isolated between specialists;
- how the residual ledger controls progress;
- how a skill file changes orchestration behavior; and
- why deterministic validation still matters in a multi-agent system.

## If You Get Stuck

Rerun the notebook from the last successful section.

If the Colab runtime resets, begin again from the setup cells near the top.

Ask the instructor for help before changing package versions, model settings, or the core lab data.

## Saving Your Work

Opening the notebook from GitHub does not modify the workshop repository.

If you want to keep your own edited copy, use Colab's **File → Save a copy in Drive** option.

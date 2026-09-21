# Lab 2 — The Agent Loop, Exposed

In this lab, you will rebuild the Morrow Peak Outfitters reconciliation investigator in plain Python so you can see the control logic that sits around the model: tools, state, the agent loop, stopping conditions, and execution safeguards.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kieDotson/tdwi-agentic-ai-workshop/blob/main/lab-2-agent-loop/lab-2-agent-loop.ipynb)

## Start Here

Click **Open in Colab** above.

Once the notebook opens:

1. Run the cells from top to bottom.
2. Enter the temporary workshop Gemini API key when prompted.
3. Read the Markdown instructions before each code section.
4. Complete the **YOUR TURN** sections when you reach them.
5. Pause at the engineering checkpoints and answer the questions before moving on.

Most of the Python is already written. The goal is to understand how reliable agents are engineered, not to write the notebook from scratch.

## Files

- `lab-2-agent-loop.ipynb` — the complete guided Lab 2 notebook
- `data/` — Finance and Sales Q3 reconciliation extracts used by the notebook

The notebook loads the lab data directly from this GitHub repository. If that fails, the notebook includes a manual upload fallback.

## What You Will Work With

During the lab, you will make the main parts of an agent harness visible:

- tool registry
- investigation state
- structured model decisions
- tool dispatch
- the control loop
- business stopping conditions
- terminal states
- maximum-step limits
- repeated-tool safeguards
- readable execution traces

You will keep the model, tools, and data largely the same while changing the control logic around them.

## If You Get Stuck

Read the explanation immediately above the cell you are working on and rerun the notebook from the last successful section.

If your Colab runtime resets, begin again from the setup cells at the top of the notebook.

Ask the instructor for help before changing package versions, model settings, or the lab data.

## Saving Your Work

Opening the notebook from GitHub does not modify the workshop repository.

If you want to keep your own edited copy, use Colab's **File → Save a copy in Drive** option.

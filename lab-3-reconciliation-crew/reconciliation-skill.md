---
name: mpo-revenue-reconciliation
version: 1.0
owner: Revenue Analytics
artifact_type: agent-skill
---

# MPO Revenue Reconciliation Skill

## Purpose

Investigate differences between Finance and Sales revenue reporting for the same business scope and reporting period.

The skill defines the investigation method. It does not grant access to data or systems.

## Trigger

Use this skill when:

- Finance and Sales report different revenue figures for the same period and business scope; and
- the difference requires investigation across reporting data, business definitions, or transformation history.

## Required Inputs

Before beginning, confirm:

- reporting period;
- business unit or reporting scope;
- Finance reported value;
- Sales reported value;
- the available evidence sources.

## Investigation Sequence

1. Confirm both reports refer to the same business scope and reporting period.
2. Compare structured transaction treatment across the reporting marts.
3. {{STEP_3}}
4. Review tickets, model changes, and transformation history if a residual remains.
5. Update the unexplained residual after every evidence-supported finding.

## Conventions

- Treat reported summary values as authoritative for the figures each team actually reported.
- Use deterministic arithmetic for the total discrepancy and remaining residual.
- Keep findings separate from hypotheses.
- Every reported cause must point to evidence that another analyst can verify.
- Do not treat an empty search result as proof that no relevant evidence exists.

## Checks

Before reporting a finding:

- confirm the amount is supported by evidence;
- confirm the finding reduces the unexplained residual;
- verify cited record or document identifiers exist;
- do not count the same cause twice.

## Definition of Done

{{DEFINITION_OF_DONE}}

## Escalation

Escalate to a human analyst when:

- available evidence is exhausted and the residual remains above the approved threshold;
- evidence sources conflict and authority cannot be resolved;
- a required source is unavailable;
- a citation cannot be verified;
- the requested scope falls outside the sources available to the agent.

## Output

Return a concise reconciliation finding containing:

- Finance reported value;
- Sales reported value;
- total discrepancy;
- each supported cause and amount;
- remaining residual;
- supporting citations;
- terminal status: `reconciled`, `unresolved`, or `escalated`.

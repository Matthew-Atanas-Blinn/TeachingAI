# Experimentation

## Purpose

`PROPOSED/` allows new ideas to be tested without modifying or later reverting the official model.

## Default state

All proposed rules are **inactive by default**. Their presence in the repository does not authorize their use.

## Activation requirements

A proposal may be used only when Matthew explicitly enables it for a named task or trial. Before use, the AI must report:

- the proposal file;
- the task or artifacts affected;
- each official rule it supplements or overrides;
- likely benefits;
- risks and possible unintended consequences;
- the success criteria for the trial.

## Override behavior

An enabled proposal may temporarily override a non-legal official standard. It may not override privacy, safety, institutional policy, or an explicit current-task instruction.

When an override is active:

1. announce it before generation;
2. apply it only within the stated scope;
3. identify it in the delivery/change report;
4. keep official files unchanged;
5. evaluate the outcome against defined success criteria.

## Proposal format

```markdown
# Proposal: Short name

Status: Draft | Ready for trial | Trial active | Accepted | Rejected
Owner: Matthew Atanas
Created: YYYY-MM-DD

## Problem
## Proposed behavior
## Official rules affected
## Scope
## Benefits
## Drawbacks and risks
## Assumptions
## Success criteria
## Trial record
## Recommendation
```

## Completion

- **Accept:** move the approved rule into the proper authoritative file, update relevant checklists and decisions, record all changes, and archive or remove the proposal as directed.
- **Revise:** keep it in `PROPOSED/` with new scope or success criteria.
- **Reject:** mark it rejected and record the reason. Retain it only if the rationale will prevent repeated reconsideration.

## Caution

Experiments can create unanticipated interactions. Therefore, do not activate all proposals globally, do not silently chain multiple proposals, and do not infer approval from prior interest in an idea.

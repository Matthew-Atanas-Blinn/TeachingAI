# Required Data Privacy and FERPA Safeguards

## Status and scope

This is operational guidance, not legal advice. Current Blinn College policy, approved contracts, and instructions from authorized institutional offices control. FERPA protects education records and personally identifiable information (PII); PII can include direct identifiers such as names or student IDs and indirect information that can identify a student.

## Operational source and verification

This file is the default operational source for routine repository work. It does not replace current institutional policy.

Do not search for legal requirements merely because they have highest authority. Research, verify, or escalate only when a material question is unresolved, current verification is required, institution-specific authorization is unknown, the local guidance may be outdated, or Matthew explicitly requests verification.

## Stop conditions

Before sending student information to an AI or third-party system, determine whether institutional use is approved and whether the system may train on, retain, redistribute, expose, or use the data outside the authorized educational purpose.

Immediately stop and report the concern if:

- the system may use submitted student data for model training;
- data retention, human review, sharing, or subprocessors are unknown or incompatible with institutional policy;
- the account or license is personal rather than an institutionally approved environment;
- student information could be exposed to unauthorized users, public repositories, logs, telemetry, or generated examples;
- the required education record is missing or inaccessible and proceeding would treat it as absent;
- there is uncertainty about whether the intended use is authorized.

Do not proceed merely because a product is paid or owned by a trusted vendor. Approval depends on the specific product, account, contractual terms, configuration, and institutional policy.

## Data-minimization rules

- Do not store student information anywhere in TeachingAI.
- Use synthetic or anonymized examples whenever actual identity is unnecessary.
- Remove names, IDs, emails, submission timestamps, accommodations, comments, and other identifiers unless the approved task requires them.
- Treat combinations of indirect details as potentially identifying.
- Use the least amount of student data needed for the authorized educational purpose.
- Grant access only to authorized people and approved systems that have a legitimate educational need for the information.
- Avoid moving records into public repositories, personal cloud storage, or unapproved AI integrations.

## Working with grades and submissions

- Use institutionally approved systems and accounts.
- Keep grade exports and submissions out of the standards repository and version control.
- If student identity is needed to merge grades, perform it only in the approved working environment and do not preserve the identifiers in reusable examples.
- If a required attachment, link, or source is unavailable, stop that student's evaluation and request the missing material rather than assigning a grade based on absence.

## Required disclosure

When a privacy risk is detected, report:

1. what information is involved;
2. the system or destination that creates concern;
3. the suspected training, retention, disclosure, or access risk;
4. what action was stopped;
5. a safer alternative, such as anonymization or an approved institutional tool.

Do not claim FERPA compliance based only on a user-interface setting or marketing statement. Escalate unresolved questions to the appropriate institutional privacy, legal, information-security, or IT authority.

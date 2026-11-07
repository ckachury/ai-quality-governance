# Governance cycle

A lightweight cycle that small product teams can run, aligned with the four functions of the NIST AI Risk Management Framework.

## Roles

| Role | Owns |
|---|---|
| Product | The policy: what the product must and must never do. Names a responsible person for each risk. |
| Development | The controls: how each rule is enforced in the system. |
| QA | The tests and the evidence: whether controls work, version by version. |
| Legal / compliance | Obligations, contracts and public texts, by market. |
| Release owner | The final decision, with residual risks accepted explicitly. |

In a small team one person can hold several roles. What cannot be skipped is **recording each decision**.

## The four steps

### 1. Govern

- Write the product policy as testable rules, each with an ID (e.g. `POL-PRIVACY-03`).
- Assign an owner to each risk and each rule.
- Agree the severity scale and the release criteria **before** testing starts.
- Keep a versioned index of the product file: scope, architecture, policy, risk register, data flows, legal matrix, test catalogue, results per version, risk acceptances, incidents.

### 2. Map

- Draw the data flow and the user journey end to end, from sign-up to account deletion.
- Identify who could be harmed: users, third parties mentioned in conversations, reviewers who see sensitive content, the organisation.
- List every place where untrusted text enters the system: forms, profile fields, uploaded documents, memory, retrieved content, previous messages.
- List vendors and what data each one receives.

### 3. Measure

- Run functional and adversarial tests on the **integrated system**, with synthetic data.
- Include long conversations, context changes, memory, failures and permitted content (to measure over-refusal, not only harm).
- Record every run with model, prompt, policy and memory versions ([release gate](release-gate.md)).

### 4. Manage

- Fix, retest and decide on residual risk.
- Record the release authorisation with open items and their owners.
- After launch: reporting channel, severity triage, ability to switch features or models off, and a regression test for every incident.
- Repeat the cycle when the model, prompts, moderation, memory or vendors change.

## Traceability unit

`risk → policy rule → control → test case → evidence → decision`

If any link is missing, the risk is not managed, whatever the documents say.

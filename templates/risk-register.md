# Risk register

One row per risk. A spreadsheet version is in [risk-register.csv](risk-register.csv).

## Fields

| Field | Description |
|---|---|
| ID | R01, R02… |
| Scenario | What could happen, written as a concrete situation |
| Who is harmed | User, third party, reviewer, organisation |
| AI RMF function | Govern · Map · Measure · Manage |
| Severity | See scale below |
| Likelihood | Low · Medium · High, **with the reason** (evidence, exposure, complexity) |
| Policy rule | The rule this risk relates to |
| Control | How the system prevents or detects it |
| Owner | A named person |
| Implementation status | Not started · In progress · Implemented · Verified |
| Tests | Test case IDs |
| Evidence | Link to execution results |
| Residual risk | After controls |
| Decision | Accept · Mitigate · Avoid (remove the feature) · Transfer |
| Review date | When it will be looked at again |

## Severity scale

| Severity | Meaning |
|---|---|
| Critical | Harm to vulnerable people, exposure of one user's data to another, or meaningful help to cause serious real-world harm |
| High | Violation of user consent or control, emotional manipulation, ineffective privacy controls, model output able to change permissions |
| Medium | Affects user control or trust without the harms above |
| Low | Minor quality issues with no safety or privacy effect |

## Rules

- Unknown is recorded as **not assessed**, never as low.
- A critical risk is not dismissed because it has not been observed yet.
- Accepted medium risks carry an owner, a justification and an expiry date.

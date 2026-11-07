# Release gate

How evaluation is run and how the release decision is made.

## Evaluation protocol

- Test the **integrated system** with test accounts and synthetic data. Never use real user conversations or real sensitive material.
- For each conversational scenario, start with **five variants and three repetitions** per variant and configuration. This is an engineering starting point to iterate on, not a statistical guarantee.
- Include multi-turn conversations and at least one close to the real context limit.
- Test every language the product launches in, plus gradual escalation and indirect phrasing.
- Repeat the affected tests whenever the model, prompts, moderation, memory or a vendor changes.

## Who judges

- Automatic evaluation helps classify results but is never the only judge.
- People review every critical failure, every ambiguous case and a sample of passes.
- Reviewers know the rubric, resolve disagreements and record them.
- Limit reviewers' exposure to distressing content.

## What is recorded for each run

Test ID and version · environment · date · model and version · parameters · policy, prompt and memory versions · synthetic inputs · output · expected vs observed · severity · verdict · reviewer · defect reference.

Evidence is stored with restricted access and a defined retention period.

## Exit criteria

- **Zero open critical or high failures** in the agreed test set. A reproduced failure needs a fix and a regression run before that version is approved.
- All authorisation, access and data-isolation tests that apply have passed.
- Legal or contractual requirements that block operation are resolved.
- Rates are reported with **numerator and denominator per category**: policy compliance, harmful content delivered, over-refusal of permitted content, invented memories, differences by language or group.
- Thresholds for non-critical metrics are agreed **before** acceptance testing starts.
- Product, development and QA record their decision; legal closes the items that apply.
- Nothing marked *not assessed* counts as passed.

## After launch

- An accessible reporting channel, severity triage and a named responder or declared coverage.
- The ability to switch off a feature or a model quickly.
- For each incident: contain, keep minimal evidence, assess communication obligations, fix, add a regression test.
- Do not claim continuous human monitoring if it does not exist.
- Review reports and metrics on an agreed cadence, without indiscriminate reading of user conversations. Exceptional access needs a purpose, permission, notice and retention rule.

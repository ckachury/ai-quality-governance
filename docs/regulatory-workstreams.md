# Regulatory workstreams

Questions a product team should resolve **with legal counsel** before launching an AI product in several markets. This is an agenda for that conversation, not legal advice and not a review of any country's law.

| Workstream | Decision to document | Evidence of closure |
|---|---|---|
| Territorial scope | Operating entity, target countries, access restrictions, applicable rules | Matrix by market with sources and a dated review |
| Data and legal basis | Purpose and legal basis for each processing activity; special care with sensitive data, memories and secondary uses | Data inventory and data-flow diagram; privacy texts and records |
| Age and access | Whether age assurance is needed, which method is proportionate, what data the provider receives and keeps | Legal and technical assessment, contract, tests |
| Rights and deletion | Requests, identity checks, timelines, export, deletion and justified exceptions | Tested procedure and retention policy per system |
| Vendors and transfers | Who receives data, where, why, for how long; sub-processors; use for model training | Contracts, verified configuration, transfer review |
| AI transparency | When and how users are told they interact with AI; obligations by role (provider or deployer) | Notice texts, placement, version recorded at acceptance |
| Content and third parties | Rules on harmful content, impersonation, third-party rights and complaint handling | Policy, reporting mechanism, specialised review |
| Model and payment contracts | Model licence, hosting and payment terms compatible with the business | Contractual approval of the chosen stack |
| Consumer protection | Promises, quotas, renewals, cancellations and charges users can understand | Reviewed terms and screens; cancellation journey tested |
| Incidents | Owners, obligations and deadlines to notify | Procedure and a simulation exercise |

## Recording each market

For each country or state: rule and article · official source · date consulted and effective date · applicability criterion · obligation · control · test · owner · opinion · next review.

A bill in progress is tracked separately from a rule in force.

## Common mistakes

- Assuming that complying with one regime (for example the GDPR) covers every other market.
- Treating a region as one jurisdiction: "Latin America" or "the United States" need country- or state-level review.
- Using language or a single IP address as proof of where a user lives.
- Calling the product "entertainment" or "fiction" and assuming that settles its legal classification.
- Hard-coding notice intervals or legal deadlines without checking the applicable rule.

## Product requirements that make compliance possible

1. Make age methods, AI notices, legal texts and territorial rules **configurable**, and store which version each user accepted.
2. Separate commercial expansion decisions from technical acceptance: a market opens when its legal and operational conditions have evidence of closure.
3. Schedule a legal review before opening countries, adding images or voice, sharing content between users, or changing how memory works.

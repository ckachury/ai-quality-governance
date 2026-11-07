# Risk catalogue for conversational AI products

A starting point for the risk register of a product where users talk to an AI assistant or character that keeps memory across sessions. Adapt severities to your product and users.

| ID | Severity | Scenario | Control | Test idea |
|---|---|---|---|---|
| R01 | Critical | A user retrieves conversations or memories from another account | Authorisation on every operation, including memory retrieval, export, duplication and deletion | Second account tries to read, edit, duplicate, export or delete someone else's data through UI and API |
| R02 | High | Data from one conversation or project leaks into another of the same user where it should not | Isolation of queries, summaries and caches per scope | Plant a unique synthetic marker in A; query B and a copy of A's settings |
| R03 | High | Text in a form field, document, memory or previous message changes the system's rules (prompt injection) | Permissions and rules enforced outside the model; untrusted input kept in separate layers | Instructions to ignore the policy in every input field, uploaded file and retrieved summary |
| R04 | High | Deleting or correcting data does not stop its future use | Deletion designed into the memory engine: history, summaries, indexes, caches, backups | Delete a memory, summarise, reopen the session and check it is not reused or restored |
| R05 | High | Analytics, error traces, notifications or support tools receive sensitive conversation content | Data inventory; no free text in analytics; restricted internal access with logging | Synthetic markers searched in logs, events, notifications and support tools |
| R06 | High | The assistant pressures users emotionally, discourages them from leaving, or ties affection or help to payment | Healthy-relationship policy; payment and quota messages come from the interface, not the character | Scenarios: user wants to leave, quota reached, subscription cancelled |
| R07 | Critical | The product gives harmful guidance to a user in a real crisis | Crisis response policy reviewed by competent people; no false promises of human intervention | Signals of real risk inside and outside a fictional frame |
| R08 | High | The assistant impersonates or produces harmful content about a real, identifiable person | Rule on real people applied to free text and conversation, with a reporting procedure | Requests involving an identifiable third party |
| R09 | High | Moderation fails open, or output is shown before it is evaluated | Safe state on failure; output checked before display, including streamed text | Moderation down, slow, partial response, retry, user stops generation mid-stream |
| R10 | High | Model output contains markup, links or instructions that execute in the interface | Output sanitisation; rate, length and concurrency limits | Output with tags, links and scripts; bursts of requests |
| R11 | Medium | Permitted content is refused unevenly across groups, or the assistant invents memories | Comparable tests across groups; memory provenance and user correction | Equivalent conversations changing only gender, origin or disability; ask about facts never stated |
| R12 | High | Model, hosting or payment vendors' terms are incompatible with the product, or they reuse user data | Vendor inventory, contracts, configuration verified, version change control | Review of terms and settings; check data-use options per vendor |
| R13 | Medium | Users are not clearly told they are talking to an AI | Visible notice before the first interaction and where the law requires it | Check notice presence, wording and version recorded at acceptance |

## Using it

1. Copy the rows that apply into the [risk register](../templates/risk-register.md).
2. Add the risks specific to your domain: what would be a wrong decision, a legal problem, a financial loss or reputational damage if the model got it wrong?
3. Mark every control **not verified** until a test produces evidence.

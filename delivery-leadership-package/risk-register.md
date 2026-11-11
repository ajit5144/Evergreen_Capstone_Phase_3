# Risk Register

> Copy to `delivery-leadership-package/risk-register.md`. At least 5 rows. **No boilerplate**; your peers will grade you on whether these are real.

| # | Risk | Owner | Likelihood (L/M/H) | Impact (L/M/H) | Mitigation | Trigger to escalate |
|---|---|---|---|---|---|---|
| R1 | The static site uses old rates and is not connected to the API| Delivery Leab| H | M | Document the mismatch and standalone site behavior; place API integration and rate alignment on the roadmap | Stakeholders treat site estimates as sponsor-approved or expect the site to save quotes.|
| R2 | Kubernetes startup or image-loading problems prevent the cluster demonstration| Deliver lead | M | H | Dry-run manifests, load the API image, deploy MongoDB first, wait for availability, and confirm three API pods plus one database pod. | The API image fails to load or required pods do not become ready within the planned demo window. |
| R3 | Missing timestamps on seeded quotes are mistaken for an API defect| Engineering Team | M | M | Explain the difference between mongosh-seeded and API-created records | Stakeholders reject seeded records because createdAt is absent |
| R4 | The temporary cluster remains running after the demonstration |Delivery Lead  | M | L | Stop port-forwarding and delete the kind cluster after the demo | The cluster remains active after planned teardown |
| R5 | Stored quotes cannot be traced to the rate version used when they were created| Data Team | M  |M  | Record rate-change decisions and commit references. For future delivery, consider storing a rate-version identifier with each quote; do not expand this week’s schema without approval. | A stakeholder asks which rate version produced a quote and the answer cannot be established |

## How I'll use this register

I’ll review this register during daily check-ins, after sponsor injects, and before go/no-go and merge decisions. I’ll update ratings, mitigations, and owners as conditions change, and escalate any risk that reaches its stated trigger

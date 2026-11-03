# Delivery Goal: Evergreen Quote


## Goal

Deliver a working Evergreen Insurance Quote API that creates and retrieves quotes through REST and GraphQL, backed by MongoDB and sponsor-approved rates. Demonstrate the service in Docker and local Kubernetes, then merge it into `main` through a reviewed pull request with passing CI checks.


## "Done" looks like
- REST endpoints retrieve quotes and create new quotes with correct premiums; invalid requests are rejected.
- GraphQL queries and mutations work through /explorer and share the same database and premium logic as REST.
- The service name is Evergreen Quote API, and sponsor-approved rates are applied: auto 90, home 135, life 70.
- All baseline tests pass, and GitHub Actions CI is green on the reviewed pull request before merge.
- The Docker image runs successfully with the expected configuration and database access.
- The local kind demonstration shows three API replicas and one MongoDB pod, with a quote created and retrieved through the Service.
- The marketing site is previewed locally, and its S3 deployment artifacts and access policies are reviewed.
- The delivery is merged into main and re-verified.
- The required leadership artifacts are completed and committed, the GitHub task board is updated, and the five-minute Friday - delivery review is ready.

## the below is old data - have to be updated ---
- The API answers every documented route: list, fetch by id, create with a computed premium.
- The same data answers through GraphQL, with the explorer at `/explorer`.
- `npm test` passes; the safety net holds.
- The containerized API serves the same answers as the dev server, and the CI run on the merge commit is **green**.
- The cluster demo shows three API pods behind one Service.
- A reviewed PR is merged, branch deleted.
- `delivery-leadership-package/` is complete and committed.

## Out of scope (this week)

- Writing application code from scratch or refactoring the supplied components.
- Features beyond the provided REST routes, GraphQL operations, and quote validation.
- Connecting the marketing site to the API or updating its rate logic; these gaps will be documented as risks or roadmap items.
- Production hardening, high availability, or durable database storage for the local cluster demonstration.
- Live S3 or EKS deployment unless explicitly approved by the instructor.
- Optional coding challenges and stretch leadership artifacts; these will not delay required delivery.

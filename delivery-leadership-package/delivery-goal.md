# Delivery Goal: Evergreen Quote

## Goal

Deliver a working Evergreen Insurance Quote API that creates and retrieves quotes through REST and GraphQL, using MongoDB and sponsor-approved rates. Demonstrate the API’s MongoDB integration with a Docker image and a local Kubernetes cluster. Publish the static marketing site to an AWS S3 bucket, then merge the reviewed changes into main after all CI checks pass.

## "Done" looks like
- REST endpoints retrieve quotes and create new quotes with correct premiums; invalid requests are rejected.
- GraphQL queries and mutations work through /explorer and share the same database and premium logic as REST.
- The service calculates and post the premium to mongodb as expected
- All baseline tests pass, and GitHub Actions CI is green on the reviewed pull request before merge.
- The Docker image runs successfully with the expected configuration and database access.
- The local kubernetes demonstration shows three API replicas and one MongoDB pod, with a quote created and retrieved through the Service.
- The marketing site is previewed locally, and its S3 deployment artifacts and access policies are reviewed.
- The delivery is merged into main and re-verified.
- The required leadership artifacts are completed and committed, the GitHub task board is updated

## Out of scope (this week)

- Features beyond the provided REST routes, GraphQL operations, and quote validation.
- Exposing the API or MongoDB as a public production service.
- Live S3 or EKS deployment
- Production-grade security, availability, scalability, and disaster recovery

# Evergreen Quote: Vision Brief

## Product
**Name:** Evergreen Quote API (Phase 3 service delivery)
**Delivery week:** 3
**Delivery Lead:** Ajit Ranjan Sahu
**Engineering team (represented by):** https://github.com/ajit5144/Evergreen_Capstone_Phase_3
**GitHub Project board:** https://github.com/ajit5144/Evergreen_Capstone_Phase_3

## Who is the customer?
People ,who are exploring auto, home, or life insurance want to create a quote and return to it later without starting over.

## What pain does Evergreen Quote remove?
Today, Evergreen calculates estimates locally but does not save them or offer a shared quote service for partner applications. Customers exploring auto, home, or life insurance need to save a quote and return to it later without starting over. Evergreen Quote should evolve from a temporary, on-screen estimator into a service that stores and retrieves quotes for customers.

## What does "good" look like at end of the week?
- REST and GraphQL create and retrieve MongoDB-backed quotes using sponsor-approved rates.
- Automated tests and PR CI pass; reviewed delivery changes are merged into main.
- The Docker image runs successfully, and local Kubernetes demonstrates three API replicas and one database pod.
- The static site is previewed and its S3 deployment artifacts reviewed.
- Required leadership artifacts are committed, and the delivery review is ready.

## What are we explicitly NOT doing this week?
- Connecting the static website to the API.
- Hosting Kubernetes cluster in Could
- Website validation with other hyperlinks like Claims and contact page

## How will we know if it worked?

- All the Test cases passes during deployment
- Docker image is built and deployed
- A quote created through the Kubernetes Service is retrieved successfully with the expected premium.

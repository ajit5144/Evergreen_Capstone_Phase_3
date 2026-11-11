## Task and Prompt

> Using this file’s existing test setup and conventions, draft one test verifying that POST `/api/quote` with `type: "auto"` and `age: 35`, but no `coverageAmount`, returns HTTP 400. Do not change application code or existing tests.


## Critique

Copilot generated a test case that followed the instructions by sending a POST request to /api/quote without coverageAmount and checking for HTTP 400. When I ran the test, the API returned the expected status, and the test passed. No incorrect behavior was observed during this run, although passing alone does not prove the test covers every scenario. I would retain the test after reviewing its request and assertions. The local test suite checks Copilot’s output against API behavior, while GitHub Actions provides the same check on repository changes. Human review remains necessary to confirm the test meaningfully verifies the requirement.

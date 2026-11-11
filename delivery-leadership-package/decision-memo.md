# Decision Memo: Inject 1

**Date:** 11/10/2026
**Author:** Ajit Ranjan Sahu
**Decision area:** Day 2 Inject

## Context

The sponsor requested renters coverage through the API by Thursday, while the platform team reported a moderate-severity vulnerability in the container’s base image. The patch is unavailable until next week, and the API is not internet-exposed this week. We must decide whether to expand scope and whether to proceed with the planned container delivery.

## Options considered

1. **Option A: Add renters coverage and proceed with the current image.**  Meets the partner’s requested date, but requires engineering to confirm rates, validation, and tests. It would require an agreed scope reduction and security approval for the current image.
2. **Option B: Defer renters coverage and proceed with a controlled lab delivery.** Protects the agreed delivery goal while allowing time to implement renters correctly. Requires a documented, time-limited security exception and a commitment to patch next week.
3. **Option C: Hold container delivery until the patch arrives.** Avoids releasing with the known vulnerability, but misses this week’s container demonstration and delays the agreed delivery.

## Recommendation

I would recommend going with Option B. Defer renters coverage and proceed with a controlled lab delivery.

Defer renters coverage to the next delivery round and retain the required scope without cutting testing or release checks. Proceed with the current base image only for the non-internet-exposed lab delivery, subject to platform/security approval of a time-limited exception. 

## Why

A dependable quote service is more valuable than meeting a new deadline with unverified coverage or accepting security risk without accountable approval.

## What would change my mind

I would revisit renters coverage if, before Thursday’s release decision, engineering supplies sponsor-approved rates, validated implementation, passing tests, and an agreed scope tradeoff that preserves the delivery goal. I would hold the container release if security approval is denied, the API becomes internet-exposed, or the vulnerability assessment indicates higher risk.


# Decision Memo: Hold Release Until Validation and Deployment Are Verified

**Date:** 11/12/2026
**Author:** Ajit Ranjan Sahu
**Decision area:** Day 3 Inject

## Context

Support reports that customers cannot obtain quotes because requests return 400 with an unexpected minimum-age requirement of 110. Separately, engineering pushed a validation hotfix to main, and its CI test step is failing. The timing suggests a possible connection, but the cause and the version serving customers are not yet confirmed.

## Options considered

1. **Option A: Continue merging while engineering investigates**  MKeeps planned delivery moving, but adds changes during an unresolved incident and bypasses the green-CI release requirement.

2. **Option B: Hold release changes and coordinate investigation and recovery** Protects customers from additional uncertainty and preserves the quality gate, but may delay the planned delivery.



## Recommendation

I would recommend going with Option B. Hold release changes and coordinate investigation and recovery

Ask the engineering incident owner to investigate the validation behavior, identify the version serving customers, and assess whether rollback or a tested correction is appropriate. Ask Support to provide representative requests, timestamps, and the affected environment, and to confirm recovery afterward. As Delivery Lead, I will coordinate updates, defer nonessential work, and request sponsor support for any schedule impact. I will not assume that the hotfix caused the incident or prescribe a code change.

## Why

Restoring customers’ ability to obtain accurate quotes takes priority over meeting the delivery schedule with an unverified release.

## What would change my mind

I would change the decision to go when the accountable engineering owner confirms recovery, valid quote requests succeed, invalid requests remain correctly rejected, and CI passes for the exact proposed release commit. Support must also confirm that the reported customer issue no longer reproduces. These checks must be completed before the next merge or deployment; otherwise, the hold remains in place.


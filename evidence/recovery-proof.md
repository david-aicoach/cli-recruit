# ARC Recovery Proof

Date: 2026-09-04

## Destructive test

1. Verified `AGENTS.md` existed as the clean-room machine-first operating contract.
2. Deliberately deleted `AGENTS.md` from the operations repository.
3. Used durable `arc-estate.json`, the target North Star/Skills references, and public ARC as recovery sources.
4. Reconstructed `AGENTS.md`.
5. Re-read the recovered file from GitHub and confirmed its routes resolve to the target North Star, Skills owner, work queue, reconnection handoff, estate snapshot and public ARC.

## Result

PASS — the ARC-owned operating surface was recoverable without private TBHRC data, chat-only state, credential values or copied external-system records.

## Independent workflow evidence

- Durable work item: https://github.com/david-aicoach/cli-recruit/issues/1
- Verified artifact: https://github.com/david-aicoach/cli-recruit/blob/main/workflows/openai-python-brief.md
- External reconnection evidence: https://github.com/david-aicoach/cli-recruit/blob/main/evidence/reconnection-proof.md
- Skills owner: https://github.com/david-aicoach/trx-poly

## Friction / hidden assumptions found

- The current ChatGPT GitHub connector can mutate repositories but does not expose repository creation. The connected-app hub has a GitHub create-repository action, but its separate GitHub OAuth connection is not active.
- To keep the proof moving without an auth pause or repurposing active projects, the test used one completely empty personal repository plus one repository that contained only a one-line README.
- This is an execution-surface limitation, not a reason to add ARC machinery. ARC's normal `gh` bootstrap repository-creation path remains covered by the existing functional code/CI contract.

## KISSS decision

No new ARC validator, health subsystem, schema or deployment service is justified by this proof.

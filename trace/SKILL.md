---
name: trace
description: On-chain forensic investigation of a crypto hack. Clusters attacker wallets, traces funding, replays the drain, and attributes with evidence. Every claim needs a tx hash; never names a person.
---

TRACE · Claude Code forensic skill
You don't guess. Every claim needs on-chain evidence: tx hash, block, address.
Label everything CONFIRMED or INFERRED. Never name a person.

0 INPUT  the incident: chains, victim wallets, time window. Save to CASE.md.

1 INGEST  pull every tx in the window from archive nodes; join Arkham, Etherscan and Chainalysis labels. Decode calldata; flag 7702 delegations.

2 CLUSTER  common-input, deposit reuse, gas funding → union-find clusters. Write clusters.json: size, flow, first seen, last seen.

3 FUNDING  walk the attacker's gas back through mixers and bridges; match every hop against 2.4M labeled addresses. Report the first labeled payer.

4 PATTERN  replay the drain order. Compare it to public balance rankings and internal events (key rotation, deploys). Mismatches are leads, not proof.

5 ORIGIN  deploy metadata, mempool first-seen relays, ASN, latency vectors. Give a location only with 3+ independent signals.

6 ATTRIBUTE  bytecode, cluster overlap, deploy + funding m.o. vs known groups (Lazarus / APT38 …). Report every match in %, never as fact.

7 REPORT  findings, confidence, timeline, sealed evidence package (sha256). Draft IC3 + exchange notices. Never send without my OK.

8 WATCH  monitor every cluster; alert exchanges on new deposits; log freezes.

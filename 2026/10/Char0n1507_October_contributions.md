# Security Reports - October 2026

## Report 1 - GHSA-mc36-c3gm-3cj4

Reported by (@Char0n1507)

Malicious indexer crashes tari_walletd via SubstateDiff id/value 
mismatch with no authentication required (CP-2). The fix was applied 
by the Tari team in tari-ootle#2813.

## Report 2 - GHSA-9795-9pp8-phgh

Reported by (@Char0n1507)

Consensus message decode expands 24-48x beyond wire-byte accounting,
leading to remote unauthenticated memory exhaustion (OOM) of validator
nodes in tari-ootle. The fix was applied by the Tari team in 
tari-ootle#2887.

## Report 3 - GHSA-96fw-3mr9-2qq2

Reported by (@Char0n1507)

Unauthenticated single-peer fill of the 64 MiB consensus future-view
buffer at the nearest view permanently locks out honest proposals and
votes in tari-ootle. The fix was applied by the Tari team in
tari-ootle#2921.

## Report 4 - GHSA-5pw5-mf52-mfj6

Reported by (@Char0n1507)

tari_indexer unauthenticated GraphQL endpoint has no per-request
complexity limit, enabling alias amplification DoS (CWE-770) in
tari-ootle. The fix was applied by the Tari team in tari-ootle#2926.

## Report 5 - GHSA-95fq-78jc-hrqp

Reported by (@Char0n1507)

Engine-op host work unmetered in WasmProcess::handle leading to 
~800x CPU amplification DoS against consensus validation in 
tari-ootle. The fix was applied by the Tari team in 
tari-ootle#2934.

## Report 5 - GHSA-3rc7-6cr6-8mx8

World-readable app config files allow cross-user MCP token theft,
secret recovery, and authenticated control-plane access in
tari-project/universe. The fix was applied by the Tari team
(config files created 0600 instead of inheriting 0644) Fixes #338.

Technical details remain in the advisory until it is published.

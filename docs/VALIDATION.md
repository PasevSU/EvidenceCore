# Validation and testing plan

No independent validation or certification is claimed for this repository snapshot.

## Minimum test matrix

1. Known-good fixtures for each advertised file format.
2. Malformed, truncated, empty and oversized fixtures.
3. Nested MIME, multipart boundaries, unexpected transfer encodings and binary attachments.
4. Valid, invalid, expired, untrusted, mismatched and revoked signing scenarios, where applicable.
5. Baseline byte hashes before/after non-destructive analysis.
6. Reproducible outputs on fixed test cases and controlled environments.
7. Safe HTML report rendering with untrusted strings.
8. Offline mode and network-denial behavior.
9. Missing-dependency errors and graceful degradation.
10. A comparison against independently implemented reference tools.

## Evidence interpretation

Each verification result must specify whether it represents parsing, calculation, signature validity, PKI trust or independent provenance. Capture exact versions and timestamps for repeatable analysis.

## Release decision

Do not declare forensic validation complete until logs and expected results for the above matrix are retained and reviewed.

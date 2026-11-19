# hAPI Report Studio integration

EvidenceCore can act as a local evidence-analysis producer for a separate hAPI Report Studio workflow.

## Proposed data flow

```
Evidence input (copy) -> EvidenceCore analysis -> report/manifest files
                                                  |
                                                  v
                                      hAPI Report Studio intake
                                                  |
                                      presentation and archiving
```

## Integration requirements

The receiving system should validate the manifest schema, the authoring tool version and every referenced artifact path. Hash all transferred files, reject path traversal and duplicate conflicting identifiers, and avoid executing report-provided code. Use explicit authorization for portal distribution.

## Cryptography

When RFC 3161 tokens or OpenTimestamps proofs are attached, maintain their original bytes. Report both the raw proof and independent verification status rather than equating a timestamp artifact with guaranteed validity.

## Privacy

Do not automatically publish analyses, attachments or confidential case evidence to public portals. Treat report templates, metadata and derived summaries as potentially sensitive.

## Status

This document defines an interface concept and safeguards. End-to-end interoperability with a deployed hAPI installation has not been verified as part of this repository publication.

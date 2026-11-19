# User guide

## Prerequisites

Use a dedicated Windows workstation with PowerShell and sufficient free disk space. Run on a *copy* of each evidence set. Some features need optional external executables; consult [Dependencies](DEPENDENCIES.md).

## Suggested invocation

```powershell
.\Read-EvidenceFile.ps1 -Path 'D:\Evidence' -Summary
.\Read-EvidenceFile.ps1 -Path 'D:\Evidence' -All -Html 'D:\Reports\evidence.html'
.\Read-EvidenceFile.ps1 -Path 'D:\Evidence' -Sidecar
```

These examples originate from the supplied package and have not been executed in this session. Check the available parameter set on the version you actually use.

## Working procedure

1. Record who supplied the evidence, its original location, and time of acquisition.
2. Copy the evidence to a read-only or otherwise controlled analysis location.
3. Compute and retain an independent baseline SHA-256 hash of each source.
4. Run the necessary evidence inspections, documenting the exact command line and environment.
5. Store generated reports separately from input evidence.
6. Verify output consistency and record any parser warnings or missing dependencies.
7. Archive original evidence, analysis outputs, and a chain-of-custody note.

## Interpretation

A `Received` header documents what a mail system recorded; it does not inherently prove that every header is authentic. DKIM validates only the message portions covered by the signature and relevant key checks. A successful hash match establishes byte-level consistency for the material compared, not sender identity. A timestamp token must be validated including imprint, signer certificate, chain/trust and relevant policy.

## Reporting

Clearly label observed bytes, computed checks, interpretations and open questions. Preserve raw samples and intermediate outputs where possible. Document the tool version and all deviations from baseline procedure.

# PasevSU EvidenceCore

**Commercial Digital Forensics & Evidence Verification Suite**

EvidenceCore is a PowerShell-based analysis and reporting toolkit for digital-evidence folders. The original project was named *ForensicTools / ForensicFiles*. This repository package retains the original forensic engine and accompanying PDF engine without asserting that the system has been independently validated or certified.

> **Commercial proprietary software.** Source availability does not grant permission to use, redistribute, resell, or publish the code. See [LICENSE.md](LICENSE.md) and [COMMERCIAL.md](COMMERCIAL.md). A payment, checkout, or license-key verification service is **not implemented** in this package.

## Features

- Recursive examination of evidence directories and individual files.
- EML header/MIME inspection, SMTP routing timelines, DKIM body/signature checks and mail metadata analysis.
- Inspection of PDF, JSON, XML, XAdES/XMLDSig, RFC 3161 timestamp tokens, OpenTimestamps, checksum files, base64 and binary content.
- Local HTML and PDF report generation and structured sidecar reports.
- Optional manifest export for downstream hAPI Report Studio workflows.
- Bulgarian and German content in the original documentation and code.

**A detection or warning is a technical indicator, not a judicial finding.** Cryptographic verification and trust validation must be distinguished from legal authorship and evidentiary weight.

## Requirements

- Windows with Windows PowerShell or a compatible PowerShell environment. Verify compatibility before production use.
- Additional executables may be required for specific operations, notably OpenSSL or OpenTimestamps helpers; see [Dependencies](docs/DEPENDENCIES.md).
- Offline analysis is possible for many formats, but DNS and blockchain validation require explicit network access when used.

## Quick start

```powershell
# Run from this directory (use a copy of your evidence)
.\Read-EvidenceFile.ps1 -Path 'D:\Evidence' -Summary
.\Read-EvidenceFile.ps1 -Path 'D:\Evidence' -All -Html 'D:\Reports\evidence.html'
.\Read-EvidenceFile.ps1 -Path 'D:\Evidence' -Sidecar
```

See [Usage](docs/USER-GUIDE.md), [Architecture](docs/ARCHITECTURE.md), [Security](docs/SECURITY.md) and the [original detailed manual](docs/ORIGINAL-README.bg.md). Original manual examples may refer to scripts that are not part of this distribution.

## Documentation

| File | Purpose |
| --- | --- |
| [User guide](docs/USER-GUIDE.md) | Inputs, commands, output and operating workflow |
| [Architecture](docs/ARCHITECTURE.md) | Core structure and module boundaries |
| [Supported formats](docs/SUPPORTED-FORMATS.md) | Analysis scope and limits |
| [Dependencies](docs/DEPENDENCIES.md) | Runtime/optional components and gaps |
| [Security](docs/SECURITY.md) | Safe handling of evidence and untrusted inputs |
| [Validation plan](docs/VALIDATION.md) | Checks before legal or production reliance |
| [hAPI integration](docs/HAPI-REPORT-INTEGRATION.md) | Original integration specification |
| [Commercial terms](COMMERCIAL.md) | Commercial licensing process and limitations |
| [License](LICENSE.md) | Proprietary licensing terms |
| [Third party notices](THIRD_PARTY_NOTICES.md) | Third-party provenance and review actions |
| [Release checklist](docs/RELEASE-CHECKLIST.md) | Checks before publishing a paid release |

## Commercial distribution

For licensing inquiries, contact the copyright holder via a GitHub issue or an officially published contact channel. Price, payment link, customer contract and activation mechanism must be set up separately and must not be assumed to exist.

© 2026 PasevSU. All rights reserved, subject to applicable third-party license obligations.
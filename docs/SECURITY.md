# Security policy and evidence safety

## Exposure

This repository is public. **Never commit** real case files, raw EML from private correspondence, private keys, passwords, tokens, API credentials, customer data, or confidential investigation notes.

## Input safety

Treat HTML, XML, PDFs, mail headers, links and archive paths as hostile. Analyze copies. Restrict execution permissions, avoid enabling macros or untrusted scripts, and never execute embedded attachments as part of file inspection.

## Network behavior

Offline analysis should be the default when evidence sensitivity requires it. DNS, certificate, blockchain, and URL checks may disclose lookup targets to third parties; run them only after affirmative authorization and logging of network effects.

## Cryptographic claims

Distinguish digest computation, signature mathematics, certificate trust, timestamp validity and legal identity. A self-signed certificate does not by itself establish third-party trust. A cryptographically valid timestamp is not equivalent to an independently established custody trail.

## Publication gates

- Secret scan and PII review
- Dependency/license inventory
- Static PowerShell analysis
- Safe parser tests with malformed and oversized files
- Offline/network-isolation checks
- Independent verification of selected report claims
- Documentation of unsupported combinations

## Reporting vulnerabilities

Open a private security advisory on GitHub if available. Do not post exploits or evidence samples containing personal data in public issues.

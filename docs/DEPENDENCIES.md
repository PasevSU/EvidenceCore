# Dependencies

## Required

- PowerShell on a compatible Windows environment; validate the specific PowerShell edition and supported OS.
- Sufficient disk, memory and rights to read the chosen evidence copies.

## Optional or feature-dependent

- OpenSSL tooling, where invoked by the supplied script.
- OpenTimestamps reader or verification tooling, where invoked.
- PDF rendering helpers and third-party JavaScript libraries when using browser-based reports.
- Network and DNS access only for explicitly requested validation operations.

The original documentation references `ots_read.py` and `Verify-Checksums.ps1`, which are **not included** in the prepared distribution. Features dependent on those files may not work until verified and restored. Consult the actual entry-point code before installation.

## Third-party attribution

See [Third-party notices](../THIRD_PARTY_NOTICES.md). Do not assume a project's proprietary license supersedes open-source rights in embedded dependencies. Verify versions, source URLs, notices and redistribution obligations before commercial shipping.

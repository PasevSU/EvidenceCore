# Architecture

EvidenceCore is a PowerShell-oriented digital evidence inspection and reporting toolkit.

## Components

- `Read-EvidenceFile.ps1`: principal evidence inspection entry point.
- `lib/ForensicPdfEngine.ps1`: PDF report implementation, packaged separately from the main script.
- `lib/html2canvas.min.js` and `lib/jspdf.umd.min.js`: third-party browser-side report dependencies (redistribution terms require review).
- `examples/`: demonstration artifacts, not trusted evidence.
- `docs/`: operational, security, and integration guidance.

## Pipeline

1. Select individual files or directories.
2. Preserve inputs and read files without intentional modification.
3. Determine supported format and select an inspection routine.
4. Analyze applicable structures, metadata, hashes, signatures, timestamps, and reported anomalies.
5. Produce structured output and human-readable reports.
6. Independently verify the results before professional or legal reliance.

This is an architectural description, not certification of runtime behavior. Review script switches and verify external-tool availability for the exact release.

## Trust boundaries

Treat source files, MIME headers, XML, HTML, filenames, and embedded URLs as untrusted input. Do not interpret network lookups, timestamp presence, or cryptographic signature validity as proof of authorship or legal admissibility. Keep evidence analysis and publication destinations logically separate.

## Planned modularization

Suggested future separation: evidence acquisition, input parsers, mail forensics, crypto verification, timestamp verification, report rendering, manifest serialization, and hAPI gateway. These are boundaries proposed for development, not a claim that every module exists as a separately deployable service.

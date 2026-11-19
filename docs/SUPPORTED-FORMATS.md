# Formats and inspection scope

The project describes analysis of:

| Material | Intended inspection |
| --- | --- |
| EML / MIME | Headers, structure, attachments, authentication indicators, routes |
| PDF | File properties and selected document/signature indicators |
| JSON | Structured data, metadata and representations |
| XML / XAdES / XMLDSig | Markup and digital-signature related structures |
| RFC 3161 artifacts | Timestamp token parsing and verification indicators |
| OpenTimestamps | Anchoring/verification indicators with optional helper tools |
| Checksums | Digest parsing and comparison |
| Base64 and binary material | Encodings and general-purpose inspection |
| Images | File-level properties and selected metadata |

**Scope is not a guarantee of full coverage.** Parsers can fail on malformed, nested, encrypted, huge, or unsupported content. Treat absent detections as inconclusive, not proof that no anomaly exists.

<p align="center"><img src="ignotvs-seal-777.png" width="96" height="96" alt="Artifex Ignotvs seal"></p>

<h1 align="center">Artifex Ignotvs</h1>
<p align="center"><em>EX SILENTIO, TUTELA.</em></p>
<p align="center"><strong>Defensive security · Digital forensics · OSINT</strong></p>
<p align="center">Small tools. Inspectable methods. Explicit boundaries.</p>

## Featured: TESTIFEX

Did that process run after the SSH login? Check the clocks before drawing a conclusion.

**[TESTIFEX](https://github.com/artifexignotvs/testifex)** is an offline terminal workbench for selected SSH/sudo logs, journal JSON and explicit process-event JSONL. In its synthetic case, a login at `00:01:30` and a process record at `00:01:45` appear ordered. A declared ±30-second process-clock error changes that ordering from certain to possible within the interval model. Follow findings to the original bytes and inspect the assumptions; neither result proves a shared SSH session or an intrusion.

[Try the synthetic field test](https://github.com/artifexignotvs/testifex/blob/main/docs/field-test.md) · [Download the 0.1.0a1 technical preview](https://github.com/artifexignotvs/testifex/releases/tag/v0.1.0a1)

## Studia

My interests span cybersecurity, OSINT, software development and ethical hacking in authorized environments. I explore them through defensive security: building small tools, testing clear assumptions and documenting the limits of each finding.

Current areas of study include secure coding, agent security, digital forensics and evidence handling. The projects below put that work into practice through log correlation, HTTP policy checks, configuration reviews, integrity manifests and saved-page analysis.

## Instrumenta

| Tool | What it does | Start here |
| --- | --- | --- |
| **[TESTIFEX](https://github.com/artifexignotvs/testifex)** | Reviews saved evidence with source-byte references, explicit clock bounds and temporal leads. | [Synthetic field test](https://github.com/artifexignotvs/testifex/blob/main/docs/field-test.md) |
| **[EXCUBITOR](https://github.com/artifexignotvs/excubitor)** | Correlates scan and authentication patterns with evidence windows in a terminal. | [Local synthetic demo](https://github.com/artifexignotvs/excubitor#try-the-local-demo) |
| **[Relatio Workbench](https://github.com/artifexignotvs/relatio-workbench)** | Brings tool reports, access reviews and investigation notes into a local case workspace. | Browser-based evidence review |
| **[Vallum HTTP](https://github.com/artifexignotvs/vallum-http)** | Audits saved or live HTTP response headers, cookie flags, transport and browser security policies. | Offline fixtures and JSON reports |
| **[Limen MCP](https://github.com/artifexignotvs/limen-mcp)** | Reviews agent server configurations for exposed credentials, risky launchers and excessive container privileges. | Local-only configuration audit |
| **[Vestigium Integrity](https://github.com/artifexignotvs/vestigium-integrity)** | Creates SHA-256 directory manifests and detects modified, missing and added entries. | Snapshot, verify, inspect differences |
| **[Lucerna OSINT](https://github.com/artifexignotvs/lucerna-osint)** | Extracts links, destination hosts and metadata from saved HTML with source hashes and line references. | Offline evidence triage |

## Relationes

[TESTIFEX preview — When a 15-second gap cannot establish order](https://artifexignotvs.hashnode.dev/testifex-preview-when-a-15-second-gap-cannot-establish-order) — A synthetic SSH-to-process review with explicit clock uncertainty and source references.

[EXCUBITOR 0.1.0 — Detection leads, in a terminal](https://artifexignotvs.hashnode.dev/excubitor-010-detection-leads-in-a-terminal) — A first run, input formats, and operational limits.

[Relatio 001 — What a matching hash proves](https://artifexignotvs.hashnode.dev/relatio-001-what-a-matching-hash-proves) — Integrity checks and the claims they can support.

[Relatio 000 — Artifex Ignotvs](https://dev.to/artifexignotvs/artifex-ignotvs-relatio-000-1856) — An opening note on tools, evidence and method.

## Principia

- **Evidence first.** Synthetic examples and regression tests accompany the tools.
- **Bounded claims.** Every project explains what it checks and what it cannot establish.
- **Local where practical.** Command-line tools use the standard library. Network activity is explicit.
- **Readable by design.** English documentation, Latin source annotations, structured output.

## In progress

These are initial releases, built to be inspected and improved. Development focuses on reproducible investigations, comparisons between checks and portable case records.

Useful contributions start with a reproducible case, a small synthetic fixture and a clear expected result. Keep private evidence and credentials out of public issues; consult each project's security policy.

<p align="center"><em>Dubita. Examina. Protege.</em></p>

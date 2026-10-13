<p align="center"><img src="assets/mark.svg" width="96" height="96" alt="Question mark"></p>

<h1 align="center">EX SILENTIO, TUTELA.</h1>
<p align="center"><strong>Defensive security · Digital forensics · OSINT</strong></p>
<p align="center">Small tools. Inspectable methods. Explicit boundaries.</p>

## Instrumenta

| Tool | What it does | Start here |
| --- | --- | --- |
| **[Vallum HTTP](https://github.com/artifexignotvs/vallum-http)** | Audits saved or live HTTP response headers, cookie flags, transport and browser security policies. | Offline fixtures and JSON reports |
| **[Limen MCP](https://github.com/artifexignotvs/limen-mcp)** | Reviews agent server configurations for exposed credentials, risky launchers and excessive container privileges. | Local-only configuration audit |
| **[Vestigium Integrity](https://github.com/artifexignotvs/vestigium-integrity)** | Creates SHA-256 directory manifests and detects modified, missing and added entries. | Snapshot, verify, inspect differences |
| **[Lucerna OSINT](https://github.com/artifexignotvs/lucerna-osint)** | Extracts links, destination hosts and metadata from saved HTML with source hashes and line references. | Offline evidence triage |

## Principia

- **Evidence first.** Synthetic examples and regression tests accompany the tools.
- **Bounded claims.** Every project explains what it checks and what it cannot establish.
- **Local where practical.** No runtime dependencies. Network activity is explicit.
- **Readable by design.** English documentation, Latin source annotations, structured output.

## In progress

These are initial releases, built to be inspected and improved. Planned work includes broader interoperability tests, saved-report comparisons and additional documented checks.

Useful contributions start with a reproducible case, a small synthetic fixture and a clear expected result. Keep private evidence and credentials out of public issues; consult each project's security policy.

<p align="center"><em>Dubita. Examina. Protege.</em></p>

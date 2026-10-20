<p align="center"><img src="ignotvs-seal-777.png" width="96" height="96" alt="Artifex Ignotvs seal"></p>

<h1 align="center">Artifex Ignotvs</h1>
<p align="center"><em>EX SILENTIO, TUTELA.</em></p>
<p align="center"><strong>Defensive security · Digital forensics · OSINT</strong></p>


## Start here: Access Assurance Lite

**After access removal, can the original credential still reach the application?**

[Access Assurance Lite](https://github.com/artifexignotvs/access-assurance-lite) records a working baseline, then checks the same credentials after your administrative change. A separate positive-control identity helps distinguish subject-specific denial from a broken service.

Public alpha. Free MIT-licensed source. Python 3.11+ on Linux. The separate commercial core remains private.

### Try the local demo

[Download `access-assurance-lite.pyz`](https://github.com/artifexignotvs/access-assurance-lite/releases/tag/v0.1.0-alpha.1), then run:

```sh
python3 access-assurance-lite.pyz demo --directory ./first-demo
```

Use a new output directory. The demo generates synthetic credentials, makes real HTTP requests to two local resources, writes evidence files and stops its server. It does not modify existing accounts.

- **VERIFIED:** the original valid subject credential is explicitly denied while both control probes succeed within the observation window.
- **RESIDUAL:** valid subject access is still observed on at least one configured resource.
- **UNKNOWN:** failure, stale data or ambiguity prevents a supported denial claim.

The demo moves through denial, restored access, an outage, failed controls and recovery. Saved evidence is historical; its hashes do not authenticate the source. These observations do not establish that every session is gone.

**For your application:** you must implement the [cooperating probe endpoint](https://github.com/artifexignotvs/access-assurance-lite/blob/main/docs/PROTOCOL.md) on the authorization path being tested. A generic HTTP 403 is insufficient. Production compatibility and independent validation remain unproven.

**How do you currently verify existing application access after offboarding?** [Share a synthetic example or demo feedback](https://github.com/artifexignotvs/access-assurance-lite/issues/new), without internal logs or credentials.

## Other work

Cybersecurity, OSINT, software development, ethical hacking and defensive security.
The current focus is access verification; these tools address related investigation tasks.

<details>
<summary>Explore the tool collection</summary>

| Project | Practical task |
| --- | --- |
| [EXCUBITOR](https://github.com/artifexignotvs/excubitor) | Correlate scan and authentication patterns in saved or live logs. |
| [Limen MCP](https://github.com/artifexignotvs/limen-mcp) | Review server configurations before launching them. |
| [TESTIFEX](https://github.com/artifexignotvs/testifex) | Investigate saved events with explicit clock uncertainty. |
| [PROBENTIUM](https://github.com/artifexignotvs/probentium) | Review conditional findings and source-byte witnesses offline. |
| [CUSTODIA](https://github.com/artifexignotvs/custodia) | Run static binary analysis within verified Linux boundaries. |
| [FRACTURA](https://github.com/artifexignotvs/fractura) | Plan access controls while preserving required service paths. |
| [LACUNA](https://github.com/artifexignotvs/lacuna) | Test how missing or degraded telemetry changes detector results. |
| [Lucerna OSINT](https://github.com/artifexignotvs/lucerna-osint) | Triage saved HTML with link inventories and source references. |
| [Vallum HTTP](https://github.com/artifexignotvs/vallum-http) | Inspect HTTP headers, cookies and transport policy. |
| [Vestigium Integrity](https://github.com/artifexignotvs/vestigium-integrity) | Compare directory manifests for changed, added and missing evidence. |
| [Relatio Workbench](https://github.com/artifexignotvs/relatio-workbench) | Organize tool reports, access reviews and investigation notes locally. |

</details>

## Field notes

[Checking the application after access removal](https://artifexignotvs.hashnode.dev/access-assurance-lite-checking-the-application-after-access-removal) · [Why a 15-second gap cannot establish event order](https://artifexignotvs.hashnode.dev/testifex-preview-when-a-15-second-gap-cannot-establish-order)

[Project overview and editions](https://artifexignotvs.github.io/access-assurance/) · [X](https://x.com/artifexignotvs) · [Bluesky](https://bsky.app/profile/artifexignotvs.bsky.social)

*Dubita. Examina. Protege.*

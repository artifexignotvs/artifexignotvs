<p align="center"><img src="ignotvs-seal-777.png" width="96" height="96" alt="Artifex Ignotvs seal"></p>

<h1 align="center">Artifex Ignotvs</h1>
<p align="center"><em>EX SILENTIO, TUTELA.</em></p>
<p align="center"><strong>Defensive security · Digital forensics · OSINT</strong></p>

I build tools to check whether a security change actually took effect.
Access removal, PHP updates and evidence review share a requirement:
an incomplete observation must remain visible.

## Latest field note: a fix accepted upstream

A PHP process-inspection gap found during RELIQUA's comparison was independently
reproduced by the `php2shell-check` maintainer. The fix and eleven regression
cases were incorporated in version 3.0.0; the maintainer's 3.0.1 follow-up
addressed another portability issue exposed by those cases.

[Read the case study](https://github.com/artifexignotvs/reliqua/blob/main/docs/UPSTREAM_CASE_STUDY.md)
· [Upstream confirmation](https://github.com/EXT-IT/php2shell-check/pull/1#issuecomment-6361957236)
· [Try the current isolated comparison](https://github.com/artifexignotvs/reliqua/blob/main/docs/FIELD_TEST.md)

That is one accepted contribution, not a claim of customer adoption. The
RELIQUA field test asks whether fresh evidence from every declared PHP node
helps your update review. It needs no production data; setup blockers and
negative feedback are welcome. The comparator's original defect is now fixed.

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
Access verification is the longer-term product direction. RELIQUA is the current
bounded field experiment; the remaining tools address related investigation tasks.

<details>
<summary>Explore the tool collection</summary>

| Project | Practical task |
| --- | --- |
| [RELIQUA](https://github.com/artifexignotvs/reliqua) | Review PHP runtime updates and require fresh reports from every declared node. |
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

[An unreadable PHP worker is not a clean result](https://github.com/artifexignotvs/reliqua/blob/main/docs/UPSTREAM_CASE_STUDY.md) ·
[Checking the application after access removal](https://artifexignotvs.hashnode.dev/access-assurance-lite-checking-the-application-after-access-removal) · [Why a 15-second gap cannot establish event order](https://artifexignotvs.hashnode.dev/testifex-preview-when-a-15-second-gap-cannot-establish-order)

[Project overview and editions](https://artifexignotvs.github.io/access-assurance/) · [X](https://x.com/artifexignotvs) · [Bluesky](https://bsky.app/profile/artifexignotvs.bsky.social)

*Dubita. Examina. Protege.*

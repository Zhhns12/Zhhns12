# Security Research — Findings Portfolio

Independent security research focused on **smart contracts**, **Rust / WASM
runtimes**, and **web application authorization**. Every finding below was
reported through the vendor's own disclosure channel, reproduced with a working
proof of concept, and validated before submission: I do not report behaviour I
cannot demonstrate.

Where a finding is still private, the technical detail is **deliberately
withheld** in line with the vendor's coordinated-disclosure policy.

---

## Published advisories (publicly verifiable)

### GHSA-cwm2-g4fh-wvf2 — StockVault: business-logic shortfall after issuer burn

| | |
|---|---|
| **Target** | `priors-agents/priors` — StockVault (Robinhood Chain, chain ID 4663) |
| **Class** | Business logic / incorrect calculation — `CWE-682` |
| **Severity** | Medium (vendor-assigned) |
| **Published** | 2026-09-30 |
| **Credit** | `Zhhns12` — *reporter* |
| **Channel** | GitHub private security advisory |
| **Verify** | https://github.com/priors-agents/priors/security/advisories/GHSA-cwm2-g4fh-wvf2 |

**Summary.** After an issuer burn, a subsequent deposit paid the earlier
positions' shortfall — the vault's accounting attributed a deficit to the wrong
party, so a later depositor absorbed a loss that did not belong to them.

---

## Under coordinated disclosure (details withheld)

These were reported through the vendor's private channel and are **not** public
yet. Names are listed for transparency about activity; no technical detail is
disclosed before the vendor's window closes.

| Target | Channel | Status |
|---|---|---|
| `tari-project/tari-ootle` (Tari Ootle bug hunt) | GitHub private advisory | 1 submitted, 1 in preparation |

---

## Submitted — awaiting vendor triage

| Target | Class | Submitted |
|---|---|---|
| `useexchange.com` | Multiple access-control / hardening findings | 2026-09-29 |

---

## Not eligible

| Target | Note |
|---|---|
| `ably.com` (REST) | Reported and **closed as a duplicate** — an independent researcher disclosed the same class on 2026-08-09. Technical merit was not disputed; no reward. Listed for completeness, not as a finding. |

---

## How I work

- **Reproduction first.** Every report ships with a proof of concept that runs
  against the pinned commit / live target. No speculative reports.
- **Deduplication before submission.** Findings are checked against published
  advisories, the vendor's known-issues list, and prior reports in the same
  codebase before they are filed.
- **Impact over location.** Severity is argued from demonstrated impact, and
  scored honestly — including downgrading my own claims when the evidence only
  supports a lower rating.
- **Disclosure discipline.** Private channels only, and nothing published before
  the vendor's coordinated-disclosure window closes.

---

## Contact

GitHub: [@Zhhns12](https://github.com/Zhhns12)

# Tester publication — 14 October 2026

Notion 0.1.0 uses only `https://mcp.notion.com/mcp` and OAuth through Grain's
shared SDK. No credentials, native worker, local server or special runtime branch.

Source tag `v0.1.0`: `401f784ec986c4bf183594549dd75eedb057cb9d`.
Registry publication: `4c857307435099e5a97d24bac985c0bd1d224496`, index 5.
The human maintainer explicitly approved this exact first-party tester candidate.
Other submissions and changed versions retain normal source-review requirements.

| Check | Result |
| --- | --- |
| Descriptor/listing/artwork doctor | Pass, 0 findings |
| Canonical descriptor pack | Pass |
| Public OAuth metadata | Pass: DCR, S256 and `none` advertised |
| CI preparation/attestation | Pass, run 38579878509 |
| Exact source/approval/provenance receiving and signing | Pass |
| Complete signed catalogue publication | Pass, run 38580862065 |
| Independent public HTTP metadata/assets/proof | Pass, 72 requests |
| Real Grain install/account/discovery/tools | Pending disposable-workspace sign-in |

Publication does not certify account permissions or every Notion tool. No Grain
application build/release was created for this package. Detailed nonsecret
operator evidence is recorded in Grain's extension progress document.

# Mainnet Acceptance-Test Results

## Test record

- **Application:** https://urban-farm.resi.works/
- **Project:** Urban Farmer — Grow to Launch, Catalyst #1100284
- **Tester:** Lloyd Duhon
- **Start time (UTC):** 2026-09-09 23:12 (screen-recorded session; transaction time provides the authoritative chain clock)
- **End time (UTC):** 2026-09-09 23:18
- **Browser/version:** Google Chrome (exact version was not captured)
- **Wallet/version:** Eternl `v2.1.7.1`
- **Wallet network:** Cardano mainnet
- **Application build/release:** `v1.0.2-mainnet` / commit `fa83073` (final source release; corrected production content verified live at 2026-09-09 23:03:31 UTC; public commit URL pending)

## Preliminary public checks — observed 2026-09-09

| Check | Result | Evidence |
|---|---|---|
| Production page responds | Pass | https://urban-farm.resi.works/ |
| API health | Pass | https://urban-farm.resi.works/api/healthz |
| Environment reports production | Pass | https://urban-farm.resi.works/api/status |
| Payment network reports mainnet | Pass | https://urban-farm.resi.works/api/payment-config |
| Cash Register deployment on mainnet | Pass | https://cardanoscan.io/transaction/f6a29d60ff5e962ba6eb20f42add8b6a1cab8e78a4408744186b57af10d29a0b |
| Season Beacon start on mainnet | Pass | https://cardanoscan.io/transaction/0b6f561320751248a133ed2162b2b8ea54e975dff42be10d1167aaa19aa2037f |
| Season Beacon finish on mainnet | Pass | https://cardanoscan.io/transaction/f9f91de4f205221dbb82bd20dec94379af686d4685662bcab5ae8eabefe34b48 |
| Filmed acceptance-test season start | Pass | https://cardanoscan.io/transaction/09e0aafbfbe9e618ca520cf8323115c21a17bd4506c99b490795da37e71dde23 |
| Filmed acceptance-test finish/anchor | Pass | https://cardanoscan.io/transaction/51c112fbc55c2c69f9b23338c613bec8026037347db285e3c81afb3c46a8b276 |
| Ten crop guides published | Pass | https://urban-farm.resi.works/api/catalog/crops |
| M4 four-video catalog mapping | Pass | See video inventory below |

## End-to-end test matrix

| ID | Test | Expected result | Result | Evidence/reference |
|---|---|---|---|---|
| T01 | Public HTTPS load | Page loads without certificate or application error | Pass | Final walkthrough and dated public-link audit |
| T02 | API health | `/api/healthz` returns `ok: true` | Pass | Dated endpoint snapshot |
| T03 | Mainnet configuration | Network is `mainnet`, payment mode is `wallet` | Pass | Dated payment-config snapshot |
| T04 | Wrong-network handling | Preprod/testnet wallet receives clear mismatch error | Not run | No testnet wallet was introduced into the production acceptance session; non-blocking negative-path regression |
| T05 | CIP-30 connection | Supported mainnet wallet connects | Pass | Final walkthrough, 00:10–00:24 |
| T06 | Signed authentication | Challenge signs; account opens without spending transaction | Pass | Final walkthrough, 00:10–00:31 |
| T07 | RESI gating | Qualifying RESI balance is detected correctly | Pass | Final walkthrough, 00:24–00:31 |
| T08 | Farm creation | Transaction verifies; creator becomes admin | Not rerun | Existing mainnet farm/admin workspace was observed; creation was not repeated during the final filmed session |
| T09 | Rack allocation | RESI payment verifies; rack/grid appears | Not rerun | Existing five-rack configuration was observed; allocation was not repeated during the final filmed session |
| T10 | Season start | RESI payment verifies; season becomes open | Pass | `09e0aafbfbe9e618ca520cf8323115c21a17bd4506c99b490795da37e71dde23`; season `e818aade-1400-49d8-9068-ca9a30f63a9d` |
| T11 | Crop guide integration | Four M4 videos load from their crop cards | Pass | Final walkthrough, 00:45–01:17; four-guide contact sheet |
| T12 | Plant crop | Open space becomes seeded | Pass | Planting `24e93663-979f-47be-b6f8-0cb4c8873bd2`; record `69ebb9f43162593ebd043b4fca29e86b7d96e0da1c9f1aea8ad6bb35ff965c7b` |
| T13 | Initial inputs | Crop becomes active/growing; record is appended | Pass | Initial-care record `13a8f2b813a7ab7e2009790119bd98ef00e9a50a608ea6afbc36f625afa09821` |
| T14 | Daily care | Daily-care data persists in timeline | Not run | The filmed run used an issue record as the additional operational event |
| T15 | Harvest | Harvest state and measurements persist; record appended | Not run | Outside the short acceptance-run crop lifecycle; workflow remains documented in the user guide |
| T16 | Pack/TLC | TLC and quantity persist; record appended | Not run | Outside the short acceptance-run crop lifecycle; workflow remains documented in the user guide |
| T17 | Season close preparation | Record stream freezes; exact anchor generated | Pass | Acceptance root `4853b5a80c1f14dfabe85f9388e36daf7ad9ceef78a9d00f40fea6eb0fb70f73`, `records:3` |
| T17a | Season Beacon finish | Finish action confirms at configured script address | Pass | `51c112fbc55c2c69f9b23338c613bec8026037347db285e3c81afb3c46a8b276`, block `13,920,400` |
| T18 | Mainnet anchoring | Transaction confirms with label 674 metadata | Pass | https://cardanoscan.io/transaction/51c112fbc55c2c69f9b23338c613bec8026037347db285e3c81afb3c46a8b276 |
| T19 | Indexing reconciliation | Retrying closing reconciles saved tx without duplicate | Not invoked | Normal close completed; no reconciliation retry was required |
| T20 | Public validation | Public `/api/verify` result matches archive and on-chain root | Pass | `actualRootHash = expectedRootHash = 85476bd4…fff12e2c`; `verified: true` |
| T21 | Raw evidence | JSON/archive is retrievable and checksum recorded | Pass | SHA-256 `3fab647b…b33e65f`; public-safe manifest in `anchor-evidence-public/` |
| T22 | Fresh-session persistence | Data remains correct after logout/login or refresh | Not rerun | Navigation between Admin and Cropchain Explorer showed the same season state; a separate logout/login cycle was not recorded |

## Transaction and object manifest

| Item | Identifier | Public explorer/evidence URL |
|---|---|---|
| Wallet authentication | Project mainnet wallet, shortened as `addr1qykr…exnng` | N/A — signed CIP-30 challenge shown in the walkthrough |
| Cash Register deployment | `f6a29d60ff5e962ba6eb20f42add8b6a1cab8e78a4408744186b57af10d29a0b` | https://cardanoscan.io/transaction/f6a29d60ff5e962ba6eb20f42add8b6a1cab8e78a4408744186b57af10d29a0b |
| Filmed acceptance start | `09e0aafbfbe9e618ca520cf8323115c21a17bd4506c99b490795da37e71dde23` | https://cardanoscan.io/transaction/09e0aafbfbe9e618ca520cf8323115c21a17bd4506c99b490795da37e71dde23 |
| Filmed acceptance finish/anchor | `51c112fbc55c2c69f9b23338c613bec8026037347db285e3c81afb3c46a8b276` | https://cardanoscan.io/transaction/51c112fbc55c2c69f9b23338c613bec8026037347db285e3c81afb3c46a8b276 |
| Filmed acceptance season | `e818aade-1400-49d8-9068-ca9a30f63a9d` | Metadata label 674 on the filmed acceptance finish transaction |
| Filmed acceptance Merkle root | `4853b5a80c1f14dfabe85f9388e36daf7ad9ceef78a9d00f40fea6eb0fb70f73` | Three-record anchor on the filmed acceptance finish transaction |
| Season Beacon start | `0b6f561320751248a133ed2162b2b8ea54e975dff42be10d1167aaa19aa2037f` | https://cardanoscan.io/transaction/0b6f561320751248a133ed2162b2b8ea54e975dff42be10d1167aaa19aa2037f |
| Season Beacon finish | `f9f91de4f205221dbb82bd20dec94379af686d4685662bcab5ae8eabefe34b48` | https://cardanoscan.io/transaction/f9f91de4f205221dbb82bd20dec94379af686d4685662bcab5ae8eabefe34b48 |
| Farm allocation | Not rerun in filmed acceptance session | Existing farm/admin state shown in walkthrough |
| Rack allocation | Not rerun in filmed acceptance session | Existing five-rack state shown in walkthrough |
| Season start | `0b6f561320751248a133ed2162b2b8ea54e975dff42be10d1167aaa19aa2037f` | https://cardanoscan.io/transaction/0b6f561320751248a133ed2162b2b8ea54e975dff42be10d1167aaa19aa2037f |
| Farm | `d86d001d-47cc-4bf1-a17f-32c96a4ba01e` | `anchor-evidence-public/acceptance-test-mainnet-evidence.json` |
| Rack | `044f157e-9c6c-47b3-bb7c-23e5961590b6` | Archive location `Rack 1`, space `S1-1` |
| Independently validated archive season | `e429bd3f-ba67-4176-9841-6299c9765643` | `17-anchor-validation-report.md` |
| Planting | `769d752f-ec4f-4d16-bf0b-337eb1330051` | Public-safe record manifest and season-summary screenshot |
| Independently validated archive Merkle root | `85476bd46c50d6f57fd70d5f56493a9e6311174428f0b17152aaf804fff12e2c` | `17-anchor-validation-report.md` |
| Season close/anchor | `f9f91de4f205221dbb82bd20dec94379af686d4685662bcab5ae8eabefe34b48` | https://cardanoscan.io/transaction/f9f91de4f205221dbb82bd20dec94379af686d4685662bcab5ae8eabefe34b48 |
| Archive retrieval payment | `cd2ca3904bd012cd9987b138970570756135ce5a3da569d85f90502b1484e622` | https://cardanoscan.io/transaction/cd2ca3904bd012cd9987b138970570756135ce5a3da569d85f90502b1484e622 |
| Original validation archive | SHA-256 `3fab647b2e25fd8b91c46c2ac92d2416d4e00da571eac3ee06ac9dbf2b33e65f` | Reproducibly retrievable through Cropchain Explorer; original retained privately because it contains a personal contact field |
| Public-safe validation bundle | Three ordered record hashes + verifier response | `anchor-evidence-public/` |

## Milestone 4 video inventory

| Crop | YouTube | Catalog status | In-app playback |
|---|---|---|---|
| Radish Microgreens | https://youtu.be/9MeYiMZ4XcY | Published | Pass |
| Sunflower Microgreens | https://youtu.be/XjtoW53t5gQ | Published | Pass |
| Butter Lettuce | https://youtu.be/oBAABR3QPiQ | Published | Pass |
| Amaranth Microgreens | https://youtu.be/QqFseKMfW1M | Published | Pass |

## Defects and resolutions

| Defect | Severity | Resolution | Retest evidence |
|---|---|---|---|
| No high-severity application defect observed | N/A | No corrective action required | Final filmed acceptance run completed and anchored on mainnet |

## Final disposition

`PASS WITH DOCUMENTED LIMITATIONS`

Statement: The Milestone 4 production path passed: public application availability, mainnet configuration, wallet connection and signed authentication, RESI-gated access, season start, four required in-app guides, planting and operational records, season close, and label-674 mainnet anchoring were demonstrated. Farm/rack creation, wrong-network handling, full crop-lifecycle harvest/pack actions, reconciliation retry, and a separate logout/login persistence cycle were not rerun during the short filmed session; they are documented as non-blocking extended-regression items rather than represented as completed tests.

# Milestone 4 Proof of Achievement — Submission Copy

## Project

- **Project:** Urban Farmer — Grow to Launch
- **Project ID:** 1100284
- **Fund/category:** Fund11 — Cardano Use Cases: Solution
- **Milestone:** 4 — Production Launch + More Videos
- **Production application:** https://urban-farm.resi.works/
- **Evidence date:** September 9, 2026 (final acceptance test completed; chain evidence independently checked September 10, 2026)

## Executive statement

Urban Farmer has been deployed at its permanent production URL and configured for Cardano mainnet. Production retains the architecture demonstrated on preprod: Season Beacon and Cash Register Aiken validators, CIP-30 wallet authentication, RESI-gated farm and season operations, an append-only Cropchain record stream, Cardano listeners, and Cardano metadata anchoring of closed-season Merkle roots. The production crop catalog contains ten published educational grow guides, including the four guides required for this milestone: Radish Microgreens, Sunflower Microgreens, Butter Lettuce, and Amaranth Microgreens.

The evidence below is organized to map each output directly to its acceptance criteria and public proof.

---

## A. Production smart contracts, listeners, sidechain, and dApp

### A — Output

A production-deployed Urban Farmer dApp, Cardano smart contracts and listeners, production-tagged Cropchain sidechain record service, and closing/anchoring workflow.

### A1 — Acceptance criteria

A reviewer can connect a Cardano mainnet wallet holding RESI, sign in, open a farm account, and perform basic platform functions such as creating a rack, opening a season, and starting a planting. The resulting activity is recorded by the production system, and a closed season can be anchored to Cardano mainnet and independently validated.

### A2 — Evidence

- Production dApp: https://urban-farm.resi.works/
- Service health: https://urban-farm.resi.works/api/healthz
- Production status: https://urban-farm.resi.works/api/status
- Public mainnet/payment configuration: https://urban-farm.resi.works/api/payment-config
- Mainnet production walkthrough: https://youtu.be/oX0RIyBBnbs
- Reviewer runbook: https://github.com/LloydDuhon/dRep/blob/main/project-catalyst/1100284/evidence/02-mainnet-reviewer-runbook.md
- Acceptance-test results: https://github.com/LloydDuhon/dRep/blob/main/project-catalyst/1100284/evidence/03-mainnet-test-results.md
- Cash Register deployment transaction: https://cardanoscan.io/transaction/f6a29d60ff5e962ba6eb20f42add8b6a1cab8e78a4408744186b57af10d29a0b
- Cash Register deployment block: `13,920,126`
- Season Beacon start transaction: https://cardanoscan.io/transaction/0b6f561320751248a133ed2162b2b8ea54e975dff42be10d1167aaa19aa2037f
- Season Beacon finish transaction: https://cardanoscan.io/transaction/f9f91de4f205221dbb82bd20dec94379af686d4685662bcab5ae8eabefe34b48
- Season-close mainnet transaction: https://cardanoscan.io/transaction/f9f91de4f205221dbb82bd20dec94379af686d4685662bcab5ae8eabefe34b48
- Closed season ID: `e429bd3f-ba67-4176-9841-6299c9765643`
- Filmed acceptance-test season start: https://cardanoscan.io/transaction/09e0aafbfbe9e618ca520cf8323115c21a17bd4506c99b490795da37e71dde23 (block `13,920,389`)
- Filmed acceptance-test finish/anchor: https://cardanoscan.io/transaction/51c112fbc55c2c69f9b23338c613bec8026037347db285e3c81afb3c46a8b276 (block `13,920,400`)
- Filmed acceptance-test season: `e818aade-1400-49d8-9068-ca9a30f63a9d`; three-record Merkle root `4853b5a80c1f14dfabe85f9388e36daf7ad9ceef78a9d00f40fea6eb0fb70f73`
- Public validation report: https://github.com/LloydDuhon/dRep/blob/main/project-catalyst/1100284/evidence/17-anchor-validation-report.md
- Public-safe record manifest and validator response: https://github.com/LloydDuhon/dRep/tree/main/project-catalyst/1100284/evidence/anchor-evidence-public
- Original archive SHA-256: `3fab647b2e25fd8b91c46c2ac92d2416d4e00da571eac3ee06ac9dbf2b33e65f`; the wallet-gated original is reproducibly retrievable through Cropchain Explorer and is not republished because it contains a personal contact field.

Reviewers can request complimentary RESI from the project team through the Milestone Module discussion or use the production RESI Cash Register. The complimentary path is recommended for milestone verification so that a reviewer is not expected to purchase tokens solely to review the evidence.

### Public configuration observed before final testing

- Network: `mainnet`
- Payment mode: `wallet`
- Anchor metadata label: `674`
- RESI asset unit: `b7c783f6304eddbdf8f0dece4715d63cb9f453be89d97c8fba155d5752455349`
- Cash Register address: `addr1w98cwkahgjl8f39muml8lnmwn0cc9unykx5hgpx8z05fvpc9ya0vu`
- Cash Register script hash: `4f875bb744be74c4bbe6fe7fcf6e9bf182f264b1a97404c713e89607`
- Cash Register deployment transaction: `f6a29d60ff5e962ba6eb20f42add8b6a1cab8e78a4408744186b57af10d29a0b`
- Cash Register deployment block: `13,920,126`
- Season Beacon address: `addr1wy90y0rfv44jxrvddzxwtxwkvahnhxul0a8vavvfs5kqnfs8g08zj`
- Season Beacon script hash: `0af23c69656b230d8d688ce599d6676f3b9b9f7f4eceb189852c09a6`
- Season Beacon start transaction/block: `0b6f561320751248a133ed2162b2b8ea54e975dff42be10d1167aaa19aa2037f` / `13,920,152`
- Season Beacon finish transaction/block: `f9f91de4f205221dbb82bd20dec94379af686d4685662bcab5ae8eabefe34b48` / `13,920,158`

**Deployment status:** Both contract `deploymentTxHash` fields are populated in the public production configuration. The Cash Register deployment is independently verified on mainnet, and the Season Beacon start and finish transactions independently prove use of the configured Season Beacon script address and hash. The finish transaction also carries metadata label `674`, anchoring season `e429bd3f-ba67-4176-9841-6299c9765643`, farm `d86d001d-47cc-4bf1-a17f-32c96a4ba01e`, three records, and Merkle root `85476bd46c50d6f57fd70d5f56493a9e6311174428f0b17152aaf804fff12e2c` under schema `fsma204-v1`.

---

## B. Production website available for testers

### B — Output

The production Urban Farmer website is publicly available for testers to sign in and perform farm and crop-management functions.

### B1 — Acceptance criteria

A reviewer can follow the documented instructions without private credentials or assistance from the project team.

### B2 — Evidence

- Production website: https://urban-farm.resi.works/
- In-app user guide: open the Documentation/User Guide within the application.
- Reviewer prerequisites and procedure: https://github.com/LloydDuhon/dRep/blob/main/project-catalyst/1100284/evidence/02-mainnet-reviewer-runbook.md
- Logged-out public-link audit: https://github.com/LloydDuhon/dRep/blob/main/project-catalyst/1100284/evidence/09-public-link-audit-2026-09-09.md
- Completed reviewer-path evidence: https://github.com/LloydDuhon/dRep/tree/main/project-catalyst/1100284/evidence/anchor-evidence-public

The production build documents wallet sign-in, farm creation, rack allocation, season creation, planting, grow logs, harvesting, packing/TLC, closing and anchoring, and Cropchain Explorer access.

---

## C. Production deployment demonstration video

### C — Output

A public YouTube video demonstrates the production deployment and its core functions.

### C1 — Acceptance criteria

The video visibly identifies Cardano mainnet, demonstrates wallet/RESI access and basic product use, shows Cropchain activity, and connects the resulting evidence to a mainnet transaction and independent validation result.

### C2 — Evidence

- Public YouTube walkthrough: https://youtu.be/oX0RIyBBnbs
- Suggested title: `Urban Farmer Mainnet Production Walkthrough | Catalyst F11 #1100284`

---

## D. Four additional educational grow guides

### D — Output

Four educational grow guides produced using the established Indoor Urban Farming format and made available on YouTube and within the production dApp.

### D1 — Acceptance criteria

A reviewer can watch all four guides. Each guide has production value and instructional flow consistent with the previously approved Broccoli Microgreens guide.

### D2 — Evidence

- Radish Microgreens: https://youtu.be/9MeYiMZ4XcY
- Sunflower Microgreens: https://youtu.be/XjtoW53t5gQ
- Butter Lettuce: https://youtu.be/oBAABR3QPiQ
- Amaranth Microgreens: https://youtu.be/QqFseKMfW1M
- Production crop catalog showing all four as published: https://urban-farm.resi.works/api/catalog/crops
- Production dApp: https://urban-farm.resi.works/ — connect a qualifying wallet, open Grow Desk, enable `Show grow guides`, and select the corresponding crop.
- Screenshot/contact sheet of the four in-app crop cards: https://github.com/LloydDuhon/dRep/blob/main/project-catalyst/1100284/evidence/anchor-evidence-public/acceptance-test-four-guide-contact-sheet.png

All four YouTube videos use on-brand thumbnails and supporting metadata. The production API catalog identifies each video as `published`.

---

## Final attestation

The project team completed the outputs described in Milestone 4 and performed the documented production acceptance test on September 9, 2026. The filmed acceptance run completed its start transaction at `23:13:13 UTC` and its finish/anchor transaction at `23:16:54 UTC`. Public application and evidence links were checked from a logged-out browser and are intended to remain publicly accessible.

# Project Catalyst 1100284 — Urban Farmer Public Evidence

**Project:** Urban Farmer — Grow to Launch  
**Fund:** Fund 11 — Cardano Use Cases: Solution  
**Project manager:** Lloyd Duhon  
**Completion date:** September 9, 2026  
**Final release:** `v1.0.2-mainnet` / commit `fa83073`

## Public deliverables

- [Production application](https://urban-farm.resi.works/)
- [Official Project Catalyst record](https://milestones.projectcatalyst.io/projects/1100284)
- [Mainnet production walkthrough](https://youtu.be/oX0RIyBBnbs)
- [Project closeout video](https://youtu.be/rsUF6AAVB28)
- [Project closeout report (PDF)](./Urban-Farmer-Grow-to-Launch-Closeout-Report.pdf)
- [Project closeout report (extended narrative)](./Urban-Farmer-Grow-to-Launch-Closeout-Report.md)
- [Final Catalyst copy/paste responses (HTML)](./Project-Catalyst-1100284-Copy-Paste-Responses.html)
- [Milestone 4 Proof of Achievement](./evidence/01-milestone-4-proof-of-achievement.md)
- [Mainnet reviewer runbook](./evidence/02-mainnet-reviewer-runbook.md)
- [Mainnet acceptance-test results](./evidence/03-mainnet-test-results.md)
- [Anchor validation report](./evidence/17-anchor-validation-report.md)
- [Public-safe anchor and acceptance evidence](./evidence/anchor-evidence-public/)
- [Dated production endpoint snapshots](./evidence/snapshots/)
- [Sanitized working package](./urban_farmer_closeout_public_package.zip)

## Mainnet acceptance evidence

The final filmed acceptance path demonstrates wallet connection and signed authentication, RESI-gated access, the farm and rack workspace, a Season Beacon start, the four Milestone 4 grow guides, planting and initial inputs, append-only Cropchain records, season closing, label-674 anchoring, Cropchain Explorer, and production documentation.

- Cash Register deployment: [transaction `f6a29d60…d29a0b`](https://cardanoscan.io/transaction/f6a29d60ff5e962ba6eb20f42add8b6a1cab8e78a4408744186b57af10d29a0b), block `13,920,126`
- Filmed season start: [transaction `09e0aafb…1dde23`](https://cardanoscan.io/transaction/09e0aafbfbe9e618ca520cf8323115c21a17bd4506c99b490795da37e71dde23), block `13,920,389`
- Filmed finish/anchor: [transaction `51c112fb…8b276`](https://cardanoscan.io/transaction/51c112fbc55c2c69f9b23338c613bec8026037347db285e3c81afb3c46a8b276), block `13,920,400`
- Acceptance season: `e818aade-1400-49d8-9068-ca9a30f63a9d`
- Metadata label: `674`
- Record count: `3`
- Schema: `fsma204-v1`
- Merkle root: `4853b5a80c1f14dfabe85f9388e36daf7ad9ceef78a9d00f40fea6eb0fb70f73`

The test disposition is **Pass with documented limitations**. Extended negative-path, new farm/rack allocation, full crop-lifecycle, reconciliation-retry, and separate logout/login tests that were not performed in the short filmed session are explicitly marked as not run rather than represented as completed.

## Independent archive validation

The public evidence also preserves an earlier closed-season validation case for season `e429bd3f-ba67-4176-9841-6299c9765643`. Its three ordered record hashes reproduce the on-chain Merkle root, and the public `/api/verify` result is `verified: true`. This complements the filmed acceptance run with independently reproduced archive evidence.

## Reviewer access

Reviewers may request complimentary RESI from the project team through the Milestone Module discussion or use the production RESI Cash Register. A reviewer should provide only a public Cardano mainnet receiving address and should never provide a seed phrase, signing key, or private key.

## Media

- [Walkthrough English captions](./media/urban-farmer-mainnet-production-walkthrough.en.srt)
- [Walkthrough thumbnail](./media/urban-farmer-mainnet-production-walkthrough-thumbnail.jpg)
- [Four-guide in-app contact sheet](./media/acceptance-test-four-guide-contact-sheet.png)
- [Acceptance-test mainnet evidence card](./media/acceptance-test-mainnet-evidence-card.png)

## Integrity and privacy

SHA-256 for `urban_farmer_closeout_public_package.zip`:

`6D39FB013F45BD914414D3DD3A141DDD1110E81C0C3C24D9E61402721E2EC2C2`

The package excludes the raw validation archive, raw screen recordings, intermediate edit frames, and personal contact information. The public walkthrough masks wallet-sensitive regions and the personal contact field visible in the raw Cropchain payload. No end-user KPI or audience statistics are included.

The public closeout report and video cross-link this evidence package. The companion HTML file contains the two remaining Project Catalyst responses—Milestone 4 and final closeout—with live links preserved for rich-text copy/paste.

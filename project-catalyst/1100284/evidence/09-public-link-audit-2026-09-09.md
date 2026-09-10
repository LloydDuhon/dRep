# Public Link Audit — 2026-09-09

The following links were fetched without authentication and returned HTTP 200.

| Evidence | Public URL | Result |
|---|---|---:|
| Production dApp | https://urban-farm.resi.works/ | 200 |
| Health endpoint | https://urban-farm.resi.works/api/healthz | 200 |
| Production status | https://urban-farm.resi.works/api/status | 200 |
| Mainnet/payment configuration | https://urban-farm.resi.works/api/payment-config | 200 |
| Crop catalog | https://urban-farm.resi.works/api/catalog/crops | 200 |
| Catalyst project page | https://projectcatalyst.io/funds/11/cardano-use-cases-solution/urban-farmer-grow-to-launch | 200 |
| Catalyst milestone page | https://milestones.projectcatalyst.io/projects/1100284 | 200 |
| Evidence repository | https://github.com/LloydDuhon/LGUrbanFarmStudio | 200 |
| Milestone 2 feedback evidence | https://github.com/LloydDuhon/LGUrbanFarmStudio/tree/main/Milestone%202 | 200 |
| Radish Microgreens video | https://youtu.be/9MeYiMZ4XcY | 200 |
| Sunflower Microgreens video | https://youtu.be/XjtoW53t5gQ | 200 |
| Butter Lettuce video | https://youtu.be/oBAABR3QPiQ | 200 |
| Amaranth Microgreens video | https://youtu.be/QqFseKMfW1M | 200 |

An HTTP result proves reachability, not functional correctness. Repeat this audit after the final walkthrough and closeout assets are published, and test reviewer-only workflows with an appropriate wallet.

## Post-deployment recheck

At `2026-09-09 22:31:33 UTC`, production served a new frontend bundle at https://urban-farm.resi.works/assets/index-C_XWHh5H.js. The prior future-token-fountain placeholder and `Preproduction controls` heading were absent. The embedded guide's published-video inventory still listed seven guides rather than all ten, so that content item remains open. The public payment configuration now includes the Season Beacon start transaction in its `deploymentTxHash` field.

The team subsequently identified the intermediate source release `v1.0.1-mainnet` at commit `6b0e091`. At `2026-09-09 22:52:11 UTC`, production still served `index-C_XWHh5H.js`; the bundle retained the seven-guide inventory. A further release was therefore required.

At `2026-09-09 23:03:31 UTC`, production served a further bundle at https://urban-farm.resi.works/assets/index-CyaNz5RH.js corresponding to the team-identified final release `v1.0.2-mainnet` / commit `fa83073`. The embedded guide explicitly listed all ten published crop guides, including Radish Microgreens, Butter Lettuce, and Amaranth Microgreens. The stale `Missing guides show Coming soon` statement was absent. All three production-documentation findings are therefore resolved.

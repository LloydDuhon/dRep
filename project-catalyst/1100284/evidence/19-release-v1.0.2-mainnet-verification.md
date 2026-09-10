# Release v1.0.2-mainnet Verification

Final source release: **`v1.0.2-mainnet`**  
Final source commit: **`fa83073`**  
Public commit/release URL: **Pending**

## Production verification

Checked: **September 9, 2026 at 23:03:31 UTC**

- Production application: https://urban-farm.resi.works/
- Frontend bundle: https://urban-farm.resi.works/assets/index-CyaNz5RH.js
- Production status: https://urban-farm.resi.works/api/status
- Payment configuration: https://urban-farm.resi.works/api/payment-config
- Crop catalog: https://urban-farm.resi.works/api/catalog/crops

The production bundle changed from `index-C_XWHh5H.js` to `index-CyaNz5RH.js`. The final release and short commit are team-supplied identifiers because those literal strings are not embedded in the minified bundle. The observable corrected content establishes that the intended documentation update reached production.

## Documentation results

| Check | Result | Live observation |
|---|---|---|
| Cash Register description | Pass | The guide describes purchasing 10,000 RESI for 100 ADA through the deployed Cash Register contract. |
| Mainnet-safe contract wording | Pass | The obsolete `Preproduction controls` heading is absent, and the guide explains the distinct mainnet Season Beacon behavior. |
| Ten-guide inventory | Pass | The guide states that all ten crop guides are published and lists all ten with their public YouTube links. |
| Milestone 4 crops present | Pass | Radish Microgreens, Sunflower Microgreens, Butter Lettuce, and Amaranth Microgreens are included. |
| Stale missing-guide statement | Pass | The prior `Missing guides show Coming soon` statement is absent. |
| Public contract configuration | Pass | Both Cash Register and Season Beacon deployment transactions are populated. |

## Disposition

The production-documentation corrections are complete. The final source release is suitable for the remaining wallet-connected acceptance testing and walkthrough capture. Add the public commit or release URL for `fa83073` to this record when the source is published or accessible to reviewers.

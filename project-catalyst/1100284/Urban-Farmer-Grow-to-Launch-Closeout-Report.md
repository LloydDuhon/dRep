# Project Closeout Report

## Name of project and project URL

**Urban Farmer — Grow to Launch**  
https://milestones.projectcatalyst.io/projects/1100284

## Project number

**1100284**

## Project manager

**Lloyd Duhon**

## Project dates

- **Started:** March 11, 2024
- **Completed:** September 9, 2026
- **Closeout report issued:** September 10, 2026

## Fund and funding

- **Fund/category:** Project Catalyst Fund11 — Cardano Use Cases: Solution
- **Approved funding:** 293,332 ADA

## Project summary

Urban Farmer was funded to complete a functional farming-management MVP that combines Cardano transactions with a scalable sidechain record architecture and professionally produced indoor-farming education. The project progressed from infrastructure and studio setup, through smart-contract and user-feedback work, to a publicly testable preproduction release and finally a production application configured for Cardano mainnet.

The completed system retains the architecture demonstrated on preprod: Season Beacon and Cash Register Aiken validators, a Cardano wallet for signed authentication and RESI-gated actions, append-only Cropchain records, and Merkle-root anchoring to Cardano. Farmers can create farms and racks, open seasons, plant crops, record care and issues, harvest and pack produce, create traceability lot codes, and close a season. At season close, the application computes a Merkle root and anchors the season summary to Cardano using metadata label 674, allowing the final record set to be independently validated against the blockchain.

The production crop catalog contains ten published educational grow guides. The final production milestone added Radish Microgreens, Sunflower Microgreens, Butter Lettuce, and Amaranth Microgreens to the previously completed guides.

## Challenge outcomes and delivery evidence

The Fund11 Cardano Use Cases: Solution category sought early blockchain startups capable of reaching Cardano testnet or MVP readiness and demonstrating a technically functional innovation that is usable on and beneficial to Cardano or a Cardano-connected service.

Urban Farmer addressed these outcomes as follows:

- **Functional MVP:** A publicly reachable production dApp was deployed at https://urban-farm.resi.works/.
- **Technical feasibility:** Wallet authentication, RESI payments, farm and season workflows, Cropchain records, and Cardano anchoring were implemented and exercised through preproduction and production testing.
- **Public usability:** The application includes user documentation, operational interfaces, Cropchain Explorer, and embedded educational content.
- **Cardano utility:** RESI-gated actions and season anchors create verifiable Cardano activity tied to a real-world agricultural traceability use case.
- **Progression from testnet:** The project demonstrated its workflow on Cardano preprod before configuring and deploying the production mainnet version.
- **First verified mainnet component:** The Cash Register deployment transaction is publicly recorded at https://cardanoscan.io/transaction/f6a29d60ff5e962ba6eb20f42add8b6a1cab8e78a4408744186b57af10d29a0b.
- **Season Beacon mainnet operation:** Start and finish actions are publicly recorded at https://cardanoscan.io/transaction/0b6f561320751248a133ed2162b2b8ea54e975dff42be10d1167aaa19aa2037f and https://cardanoscan.io/transaction/f9f91de4f205221dbb82bd20dec94379af686d4685662bcab5ae8eabefe34b48.
- **Final filmed acceptance run:** A second mainnet season was opened and closed during the production walkthrough. Its start transaction is https://cardanoscan.io/transaction/09e0aafbfbe9e618ca520cf8323115c21a17bd4506c99b490795da37e71dde23 and its finish/anchor transaction is https://cardanoscan.io/transaction/51c112fbc55c2c69f9b23338c613bec8026037347db285e3c81afb3c46a8b276.

Final delivery evidence:

| Delivered outcome | Result | Evidence |
|---|---|---|
| Public production MVP | **Delivered** | https://urban-farm.resi.works/ |
| Cash Register mainnet deployment | **Confirmed** | Transaction `f6a29d60…d29a0b`, block `13,920,126` |
| Season Beacon start and finish | **Confirmed** | Transactions `0b6f5613…aa2037f` and `f9f91de4…fe34b48` |
| Mainnet acceptance test | **Pass with documented limitations** | Wallet authentication, RESI access, season start, four in-app guides, planting, records, close, and anchor completed September 9, 2026; see the public test-results document |
| Mainnet season anchor | **Confirmed and independently validated** | https://cardanoscan.io/transaction/f9f91de4f205221dbb82bd20dec94379af686d4685662bcab5ae8eabefe34b48; public verifier returned `verified: true` |
| Filmed acceptance-test anchor | **Confirmed** | Transaction `51c112fb…8b276`, block `13,920,400`; label `674`, three records, root `4853b5a8…fb70f73` |
| Published long-form crop guides | **10 delivered** | https://urban-farm.resi.works/api/catalog/crops |
| Required Milestone 4 crop guides | **4 delivered** | Radish, Sunflower, Butter Lettuce, and Amaranth public YouTube links |
| Recorded feedback sessions | **4 delivered** | https://github.com/LloydDuhon/LGUrbanFarmStudio/tree/main/Milestone%202 |
| Educational crop-guide runtime | **Approximately 189.9 minutes delivered** | Ten public crop-guide watch pages |

This closeout reports completed deliverables and technical verification. It does not include post-launch end-user counts, usage analytics, transaction-volume statistics, or audience-view statistics.

## Key achievements

- Delivered a farm-management MVP covering farm/rack setup, seasonal operations, planting, daily care, issues, loss, harvest, packing, and traceability lot codes.
- Implemented wallet-signed authentication and RESI-gated production actions.
- Implemented append-only Cropchain records and cryptographic season summaries anchored to Cardano.
- Provided public validation evidence linking a closed season to its on-chain anchor.
- Published ten crop-education videos and integrated them into the crop workflow.
- Conducted four structured feedback sessions with farmers and non-farmers and revised the initial Broccoli Microgreens guide based on that feedback.
- Established a professional video-production workflow and a consistent Living Greens educational brand.

## Collaboration and engagement

The team combined software architecture, full-stack development, farming expertise, and media production. Farmer and non-farmer feedback sessions were recorded during Milestone 2, with survey responses retained as public evidence. Feedback led to clearer demonstrations, improved instructional flow, revised footage, color correction, stronger audio consistency, and more useful chaptering.

The educational media and project documentation were produced through the following collaboration:

- **On-screen talent:** Melannie Duhon and Sami Doherty
- **Camera operators:** Lloyd Duhon, Gage Kroyer, Andrew Liakohvich, Jamaal Rolle, and Tyler Norman
- **Production:** Monty Tilton, Gage Kroyer, and Tyler Norman
- **Executive producer:** Melannie Duhon
- **Director:** Lloyd Duhon
- **Farm production:** Courtesy of Living Greens Urban Farm
- **Technicians:** Tyler Norman and Monty Tilton
- **Editing:** Andrew Liakohvich, Jaaziel “Jazz” Ampit, Laurena Etienne, Laurelyn Long, and Lloyd Duhon
- **Graphics:** Andrew Liakohvich, Jonathan Fenton, and Laurena Etienne

## Key learnings

- **Reviewer-verifiable evidence matters as much as implementation.** Public transaction links, raw validation data, and narrated walkthroughs make complex infrastructure understandable and independently reviewable.
- **Batching operational evidence is practical.** Recording detailed farm activity off-chain and anchoring a deterministic Merkle root at season close limits on-chain cost while preserving tamper-evident verification.
- **Wallet and indexer UX requires explicit recovery states.** A Cardano transaction may confirm before an indexing provider reports it. Persisting the submitted transaction and supporting idempotent reconciliation prevents accidental duplicate submissions.
- **Agricultural education benefits from user testing.** Feedback from both experienced farmers and non-farmers improved clarity, pacing, audio, visuals, and task ordering.
- **Technical and media pipelines require different production rhythms.** Coordinating software milestones with crop-growing and video-production schedules required more time than the original four-month estimate.

Production retained the preproduction design, including the Season Beacon and Cash Register Aiken validators, append-only Cropchain records, and Merkle-root anchoring. This continuity reduced migration risk and allowed the same validation model proven on preprod to be carried into mainnet testing.

## Scope and items not achieved

The original proposal aspired to produce fifteen crop guides. The final public catalog contains ten professionally produced long-form guides. This was the only original aspiration not fully realized. The reviewed Statement of Milestones defined the accepted educational deliverable set, including the four guides required for the final production milestone, and those milestone deliverables were completed. The project does not claim that fifteen guides were produced; additional professional indoor-crop guides remain part of the post-funding roadmap.

The original proposal used broader Cosmos/IOHK sidechain language to describe the intended scalable record and verification layer. By the approved Milestone 3 preproduction release, the implemented evidence model was documented as Cropchain append-only records, Season Beacon and Cash Register Aiken validators, and Merkle-root anchoring to Cardano. That approved implementation was carried into the production mainnet release without an architectural change.

## Next steps

- Maintain and monitor the production service and Cardano integration.
- Use the extended period before the FDA Food Traceability Rule's July 2028 enforcement horizon to prepare Urban Farmer's traceability workflows, documentation, and classroom materials.
- Continue adding professionally produced guides for additional indoor crops.
- Focus product development on Living Greens classroom grow kits and enable older students using those kits to document and track their grows through the Urban Farmer application.
- Develop classroom-friendly onboarding, permissions, and reporting so educators can supervise student activity while students learn crop management and food traceability.
- Recruit classroom and farmer pilots and collect qualitative usability feedback.
- Improve the RESI acquisition path, educator-facing reporting, and public validation experience.

The FDA states that the original Food Traceability Rule compliance date was January 20, 2026, that it proposed a 30-month extension to July 20, 2028, and that Congress directed the agency not to enforce the rule before that later date. Urban Farmer will use this preparation window to align the application and classroom program with emerging traceability needs rather than representing the product as a compliance guarantee.

## Final thoughts

Urban Farmer demonstrates how Cardano can support a real-world agricultural workflow without placing every operational event directly on-chain. The production MVP combines practical crop management and education with verifiable season-level blockchain evidence. The project closes with a public application, a repeatable verification model, and a clear path toward classroom and farmer use during the extended traceability-rule preparation period.

## Relevant project sources

- Production application: https://urban-farm.resi.works/
- Production health: https://urban-farm.resi.works/api/healthz
- Production status: https://urban-farm.resi.works/api/status
- Mainnet/payment configuration: https://urban-farm.resi.works/api/payment-config
- Published crop catalog: https://urban-farm.resi.works/api/catalog/crops
- Project Catalyst page: https://projectcatalyst.io/funds/11/cardano-use-cases-solution/urban-farmer-grow-to-launch
- Milestone record: https://milestones.projectcatalyst.io/projects/1100284
- Public closeout evidence repository: https://github.com/LloydDuhon/dRep/tree/main/project-catalyst/1100284
- Original project media repository: https://github.com/LloydDuhon/LGUrbanFarmStudio
- Milestone 3 walkthrough: https://youtu.be/0cFFuzFOVGk
- Milestone 4 production walkthrough: https://youtu.be/oX0RIyBBnbs
- Project closeout video: https://youtu.be/rsUF6AAVB28
- Cash Register mainnet deployment: https://cardanoscan.io/transaction/f6a29d60ff5e962ba6eb20f42add8b6a1cab8e78a4408744186b57af10d29a0b
- Season Beacon mainnet start: https://cardanoscan.io/transaction/0b6f561320751248a133ed2162b2b8ea54e975dff42be10d1167aaa19aa2037f
- Season Beacon mainnet finish: https://cardanoscan.io/transaction/f9f91de4f205221dbb82bd20dec94379af686d4685662bcab5ae8eabefe34b48
- Filmed acceptance-test start: https://cardanoscan.io/transaction/09e0aafbfbe9e618ca520cf8323115c21a17bd4506c99b490795da37e71dde23
- Filmed acceptance-test finish/anchor: https://cardanoscan.io/transaction/51c112fbc55c2c69f9b23338c613bec8026037347db285e3c81afb3c46a8b276
- Archive retrieval payment: https://cardanoscan.io/transaction/cd2ca3904bd012cd9987b138970570756135ce5a3da569d85f90502b1484e622
- Anchor validation report: https://github.com/LloydDuhon/dRep/blob/main/project-catalyst/1100284/evidence/17-anchor-validation-report.md
- FDA Food Traceability Rule: https://www.fda.gov/food/food-safety-modernization-act-fsma/fsma-final-rule-requirements-additional-traceability-records-certain-foods

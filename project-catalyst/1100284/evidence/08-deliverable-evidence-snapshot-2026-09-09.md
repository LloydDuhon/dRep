# Deliverable Evidence Snapshot — 2026-09-09

This dated inventory documents delivered project outputs. It intentionally excludes end-user counts, product-usage analytics, transaction-volume statistics, and audience-view statistics.

## Production service

- Production application: https://urban-farm.resi.works/
- Health endpoint: https://urban-farm.resi.works/api/healthz
- Mainnet configuration: https://urban-farm.resi.works/api/payment-config
- Published crop catalog: https://urban-farm.resi.works/api/catalog/crops

The service identifies itself as the production environment, the payment configuration identifies Cardano mainnet, and the crop catalog contains ten published crop guides. These endpoint observations establish deployment state but do not replace the final end-to-end acceptance test.

First verified mainnet contract evidence:

- Cash Register transaction: `f6a29d60ff5e962ba6eb20f42add8b6a1cab8e78a4408744186b57af10d29a0b`
- Cardanoscan: https://cardanoscan.io/transaction/f6a29d60ff5e962ba6eb20f42add8b6a1cab8e78a4408744186b57af10d29a0b
- Mainnet block: `13,920,126`
- UTC timestamp: `2026-09-09 21:36:19`
- Output `#0`: `3 ADA` at the configured Cash Register script address with datum hash `75b511c9a25dce38388fd9829f6ba2d8b00ca9ecbef1d91e3e62d5afd74b0651`

Verified Season Beacon operational evidence:

- Start: https://cardanoscan.io/transaction/0b6f561320751248a133ed2162b2b8ea54e975dff42be10d1167aaa19aa2037f — block `13,920,152`
- Finish: https://cardanoscan.io/transaction/f9f91de4f205221dbb82bd20dec94379af686d4685662bcab5ae8eabefe34b48 — block `13,920,158`
- Both transactions create output `#0` with `3 ADA` at the configured Season Beacon address and matching script credential.
- The finish transaction contains metadata label `674` with season `e429bd3f-ba67-4176-9841-6299c9765643`, farm `d86d001d-47cc-4bf1-a17f-32c96a4ba01e`, three records, Merkle root `85476bd46c50d6f57fd70d5f56493a9e6311174428f0b17152aaf804fff12e2c`, and schema `fsma204-v1`.

Verified archive and validation evidence:

- Archive retrieval transaction: https://cardanoscan.io/transaction/cd2ca3904bd012cd9987b138970570756135ce5a3da569d85f90502b1484e622
- Retrieval block: `13,920,196`
- Retrieval payment: `1,000 RESI` to the configured project receiving address
- Original archive SHA-256: `3fab647b2e25fd8b91c46c2ac92d2416d4e00da571eac3ee06ac9dbf2b33e65f`
- All three `prevRecordHash` links match the preceding record.
- Independent local Merkle result: `85476bd46c50d6f57fd70d5f56493a9e6311174428f0b17152aaf804fff12e2c`
- Public `POST /api/verify`: `verified: true`, with identical actual and expected roots.

## Educational library

| Crop guide | Duration | URL |
|---|---:|---|
| Amaranth Microgreens | 35:53 | https://youtu.be/QqFseKMfW1M |
| Basil | 11:42 | https://youtu.be/3OlWZqFJHLs |
| Broccoli Microgreens | 12:41 | https://youtu.be/GCGBz2XUhi8 |
| Butter Lettuce | 40:55 | https://youtu.be/oBAABR3QPiQ |
| Dill | 19:45 | https://youtu.be/9cPZsvzPx3w |
| Mixed Microgreens | 9:10 | https://youtu.be/iNmYwffi0VY |
| Radish Microgreens | 21:39 | https://youtu.be/9MeYiMZ4XcY |
| Romaine Lettuce | 10:24 | https://youtu.be/Ka2d2pAEkgc |
| Sunflower Microgreens | 19:39 | https://youtu.be/XjtoW53t5gQ |
| Teen Mixed Lettuce | 8:05 | https://youtu.be/SVBKKKpMHgI |

Delivered educational outputs:

- Ten public long-form crop guides
- Approximately 189.9 minutes of educational programming
- All four Milestone 4 guides public and integrated into the production crop catalog
- Four recorded Milestone 2 feedback sessions with supporting evidence at https://github.com/LloydDuhon/LGUrbanFarmStudio/tree/main/Milestone%202

## Closeout policy

The closeout report and video will describe delivered outputs and technical verification only. They will not publish or characterize end-user adoption, wallet/account totals, farm activity totals, transaction-volume totals, or audience-view statistics.

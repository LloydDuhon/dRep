# Season Beacon Mainnet Evidence

Verified 2026-09-09.

## Start transaction

- Transaction: `0b6f561320751248a133ed2162b2b8ea54e975dff42be10d1167aaa19aa2037f`
- Cardanoscan: https://cardanoscan.io/transaction/0b6f561320751248a133ed2162b2b8ea54e975dff42be10d1167aaa19aa2037f
- Block: `13,920,152`
- Block hash: `93644c359ad89e94c8d97138bbc79192d721f8f08760b81dcb7945a9f3a1891d`
- Absolute slot: `197424144`
- Timestamp: `2026-09-09 21:47:15 UTC`
- Output `#0`: `3 ADA` at the configured Season Beacon address
- Datum hash: `fea4692b45009db86ba998380668c2d0e0cb73c15c87b49edaf16854666b9730`

## Finish transaction

- Transaction: `f9f91de4f205221dbb82bd20dec94379af686d4685662bcab5ae8eabefe34b48`
- Cardanoscan: https://cardanoscan.io/transaction/f9f91de4f205221dbb82bd20dec94379af686d4685662bcab5ae8eabefe34b48
- Block: `13,920,158`
- Block hash: `3f0b93ed13b0d86075a52c2b9ec002062c95eed0e85b069cc1676b9a655b5acf`
- Absolute slot: `197424232`
- Timestamp: `2026-09-09 21:48:43 UTC`
- Output `#0`: `3 ADA` at the configured Season Beacon address
- Datum hash: `c5461c75c8fd62da084abdd5620dd8f3655639e5656f91e594d3bb716c7c6283`

## Script match

Both transactions create output `#0` at:

- Address: `addr1wy90y0rfv44jxrvddzxwtxwkvahnhxul0a8vavvfs5kqnfs8g08zj`
- Payment credential/script hash: `0af23c69656b230d8d688ce599d6676f3b9b9f7f4eceb189852c09a6`

Those values exactly match the Season Beacon configuration exposed by https://urban-farm.resi.works/api/payment-config. The API now publishes the start transaction as the Season Beacon `deploymentTxHash`; together, the start and finish transactions provide authoritative mainnet operational evidence.

## Confirmed Cropchain anchor

The finish transaction contains metadata label `674`:

- Message: `Urban Farmer Cropchain anchor v1`
- Season: `e429bd3f-ba67-4176-9841-6299c9765643`
- Farm: `d86d001d-47cc-4bf1-a17f-32c96a4ba01e`
- Merkle root: `85476bd46c50d6f57fd70d5f56493a9e6311174428f0b17152aaf804fff12e2c`
- Record count: `3`
- Schema: `fsma204-v1`

The finish transaction therefore provides both Season Beacon operational proof and the required mainnet Cropchain anchor. The downloaded archive, ordered record hashes, local Merkle calculation, and public application verifier all match these on-chain values; see [`17-anchor-validation-report.md`](17-anchor-validation-report.md).

## Preserved evidence

- [`snapshots/2026-09-09-season-beacon-mainnet.json`](snapshots/2026-09-09-season-beacon-mainnet.json)

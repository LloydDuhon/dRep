# Mainnet Cropchain Anchor Validation Report

Validated 2026-09-09 for Project Catalyst Fund11 project `1100284`.

## Result

**PASS — the downloaded Cropchain archive, its three-record hash chain, the independently recalculated Merkle root, the production verifier response, and Cardano metadata label `674` all agree.**

## Anchored season

- Season ID: `e429bd3f-ba67-4176-9841-6299c9765643`
- Farm ID: `d86d001d-47cc-4bf1-a17f-32c96a4ba01e`
- Season state: `anchored`
- Open transaction: https://cardanoscan.io/transaction/0b6f561320751248a133ed2162b2b8ea54e975dff42be10d1167aaa19aa2037f
- Anchor transaction: https://cardanoscan.io/transaction/f9f91de4f205221dbb82bd20dec94379af686d4685662bcab5ae8eabefe34b48
- Anchor block: `13,920,158`
- Anchor slot: `197424232`
- Anchored at: `2026-09-09 21:48:43 UTC`
- Record count: `3`
- Schema: `fsma204-v1`
- Merkle root: `85476bd46c50d6f57fd70d5f56493a9e6311174428f0b17152aaf804fff12e2c`

## Archive retrieval

- Retrieval transaction: https://cardanoscan.io/transaction/cd2ca3904bd012cd9987b138970570756135ce5a3da569d85f90502b1484e622
- Retrieval block: `13,920,196`
- Retrieval block hash: `06210439ae34101a17e2fab107b6b511ba8726a1dd568e6de1e6aeae21bfc8bb`
- Retrieval slot: `197425270`
- Retrieval time: `2026-09-09 22:06:01 UTC`
- Retrieval payment: `1,000 RESI`
- Original downloaded archive SHA-256: `3fab647b2e25fd8b91c46c2ac92d2416d4e00da571eac3ee06ac9dbf2b33e65f`

The retrieval transaction output `#0` pays exactly `1,000 RESI` plus minimum ADA to the project receiving address configured by the production application.

## Ordered record-hash chain

| Order | CTE type | Record hash | Previous-link result |
|---:|---|---|---|
| 1 | `planting` | `23552e4bcf5c32ebb6d7690bb5454d6363d0c25a112055ae6d8f211e901eaa81` | Genesis record; `prevRecordHash` is null |
| 2 | `initial_care` | `41cdbc394fe9173e77c84389d6425a5ae217857d8cd625d58fbbadf3a6c4ddeb` | Matches record 1 |
| 3 | `issue` | `6fa699595910569085c1a930693332fb32e4448a00dcf45e5c756f6c50e0bd2c` | Matches record 2 |

All previous-hash links passed.

## Independent Merkle calculation

The local calculation used the application's documented three-leaf procedure: concatenate each pair of lowercase hexadecimal record-hash strings as UTF-8, hash the concatenation with SHA-256, duplicate the final unpaired node, and repeat until one root remains.

Calculated root:

`85476bd46c50d6f57fd70d5f56493a9e6311174428f0b17152aaf804fff12e2c`

This exactly matches the archive's `rootHash`, archive `computedRootHash`, and Cardano metadata label `674`.

## Production verifier

The ordered record hashes were submitted to public endpoint:

`POST https://urban-farm.resi.works/api/verify`

Response:

```json
{
  "actualRootHash": "85476bd46c50d6f57fd70d5f56493a9e6311174428f0b17152aaf804fff12e2c",
  "expectedRootHash": "85476bd46c50d6f57fd70d5f56493a9e6311174428f0b17152aaf804fff12e2c",
  "verified": true
}
```

## Privacy treatment

The original downloaded archive contains a personal contact field and internal account identifiers, so it is retained locally and is not included in the public evidence repository. The publishable bundle contains its SHA-256 checksum, ordered record hashes, verifier response, retrieval transaction, and screenshots without reproducing that personal contact field. Reviewers can independently retrieve the original archive through the production Cropchain Explorer using a wallet that holds RESI.

## Public evidence files

- [`anchor-evidence-public/01-cropchain-season-summary.png`](anchor-evidence-public/01-cropchain-season-summary.png)
- [`anchor-evidence-public/02-wallet-anchor-metadata.png`](anchor-evidence-public/02-wallet-anchor-metadata.png)
- [`anchor-evidence-public/record-hashes.json`](anchor-evidence-public/record-hashes.json)
- [`anchor-evidence-public/public-verify-response.json`](anchor-evidence-public/public-verify-response.json)
- [`anchor-evidence-public/retrieval-evidence.json`](anchor-evidence-public/retrieval-evidence.json)
- [`anchor-evidence-public/SHA256SUMS.txt`](anchor-evidence-public/SHA256SUMS.txt)

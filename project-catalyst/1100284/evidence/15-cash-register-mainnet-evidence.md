# Cash Register Mainnet Deployment Evidence

Verified 2026-09-09.

## Canonical transaction

- Transaction hash: `f6a29d60ff5e962ba6eb20f42add8b6a1cab8e78a4408744186b57af10d29a0b`
- Cardanoscan: https://cardanoscan.io/transaction/f6a29d60ff5e962ba6eb20f42add8b6a1cab8e78a4408744186b57af10d29a0b
- Mainnet block: `13,920,126`
- Block hash: `455a720ac281b67c6143de0042268b29ef048e4d75c6af6eb6be1c8f1970ffcf`
- Epoch: `654`
- Absolute slot: `197423488`
- Timestamp: `2026-09-09 21:36:19 UTC`

## Script-output match

Transaction output `#0` contains:

- Value: `3,000,000 lovelace` (`3 ADA`)
- Address: `addr1w98cwkahgjl8f39muml8lnmwn0cc9unykx5hgpx8z05fvpc9ya0vu`
- Payment credential/script hash: `4f875bb744be74c4bbe6fe7fcf6e9bf182f264b1a97404c713e89607`
- Datum hash: `75b511c9a25dce38388fd9829f6ba2d8b00ca9ecbef1d91e3e62d5afd74b0651`

The address and payment credential exactly match the Cash Register values exposed by the production application at https://urban-farm.resi.works/api/payment-config. This is the first confirmed component of the Urban Farmer production mainnet deployment.

## Preserved evidence

- [`snapshots/2026-09-09-cash-register-deployment.json`](snapshots/2026-09-09-cash-register-deployment.json)
- [`snapshots/2026-09-09-payment-config.json`](snapshots/2026-09-09-payment-config.json)

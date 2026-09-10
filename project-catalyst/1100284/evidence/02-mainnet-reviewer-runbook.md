# Urban Farmer Mainnet Reviewer Runbook

This runbook provides a reproducible path for reviewing Urban Farmer on Cardano mainnet.

## 1. Prerequisites

- Desktop browser with a supported CIP-30 Cardano wallet extension, such as Eternl.
- Wallet network set to **Cardano mainnet**.
- Sufficient ADA for Cardano transaction fees and minimum-ADA outputs.
- RESI in the connected wallet.

The production application currently documents these RESI requirements:

- Any Cardano wallet can sign in.
- Any wallet holding RESI can access Cropchain Explorer.
- Creating/opening a farm and allocating a rack requires `1000.000000 RESI` per rack.
- Starting a season costs `100.000000 RESI` and requires a balance greater than `100.000000 RESI`.
- Downloading a closed-season archive costs `1000.000000 RESI`.

For a clean farm-plus-season test, use a wallet with **more than 1100 RESI** plus sufficient ADA. Confirm the exact recommended balance after production testing.

### RESI acquisition

Two paths are available:

1. **Recommended for Catalyst review — request complimentary RESI.** Send the project team a Cardano mainnet receiving address through the Milestone Module discussion. The team can provide enough complimentary RESI to complete the reviewer path. A reviewer should provide only a public receiving address—never a wallet seed phrase, signing key, or private key.
2. **Self-service — use the production RESI Cash Register.** The public production configuration defines a purchase of `10,000.000000 RESI` for `100 ADA`. Review the displayed transaction carefully before signing and confirm that the Cash Register is shown as active in the production interface.

For the milestone review, complimentary RESI is preferred because it avoids asking reviewers to spend 100 ADA merely to verify the funded deliverable.

## 2. Confirm the production environment

1. Open https://urban-farm.resi.works/.
2. Confirm the browser shows HTTPS with no certificate warning.
3. Open https://urban-farm.resi.works/api/payment-config in another tab.
4. Confirm `network` is `mainnet` and `paymentMode` is `wallet`.
5. Open https://urban-farm.resi.works/api/healthz and confirm `{"ok":true}`.

Expected result: the website and API are reachable, healthy, and configured for Cardano mainnet.

## 3. Sign in

1. Select `Continue with Eternl` or another detected CIP-30 wallet.
2. Approve the wallet connection.
3. Sign the login challenge.
4. Do not submit a spending transaction merely to authenticate.

Expected result: the application verifies wallet ownership and displays the authenticated workspace.

Capture:

- Screenshot showing successful login and a shortened/partially redacted wallet address.
- Wallet name and version.
- Browser and version.

## 4. Create a farm and rack

1. Begin first-time setup.
2. Enter a farm name, admin contact, location, rack count, shelves per rack, and spaces per shelf.
3. Review the RESI allocation transaction.
4. Sign and submit the transaction.
5. Wait for backend verification and indexing.
6. Confirm the farm and rack appear in Grow Desk.

Expected result: the wallet that created the farm becomes farm admin, and the paid rack becomes available.

Capture:

- Transaction hash and Cardanoscan link.
- Farm ID and rack ID.
- Screenshot of the completed rack grid.

## 5. Start a season

1. Open Admin → Season management.
2. Select the active farm and rack.
3. Enter a clear season label and dates.
4. Approve the `100.000000 RESI` season-start transaction.
5. Wait for backend verification.

Expected result: the season status becomes open and Grow Desk becomes the primary workspace.

Capture:

- Season-start transaction hash and Cardanoscan link.
- Season ID and season label.
- Screenshot showing the open season.

## 6. Start a planting and confirm educational content

1. Select an open rack space.
2. Choose one of the four Milestone 4 crops.
3. Confirm the crop card shows medium, environment, expected yield, and a published grow guide.
4. Play enough of the embedded guide to demonstrate that it loads inside the dApp.
5. Create the planting.
6. Enter required initial-input weights and submit.

Expected result: the space moves from `Open` to `Seeded` and then to `Growing`, and Cropchain contains the corresponding records.

Repeat the embedded-video check for:

- Radish Microgreens
- Sunflower Microgreens
- Butter Lettuce
- Amaranth Microgreens

Capture:

- Planting ID and selected rack space.
- Screenshot of the planted space.
- Screenshot/contact sheet showing all four embedded guides.
- Cropchain record IDs for planting and initial inputs.

## 7. Exercise the lifecycle

For a complete evidence season, use test data clearly labeled as an acceptance test.

1. Add a daily-care entry.
2. Add an issue entry if desired.
3. Harvest the test crop with the required measurements.
4. Pack it using a clearly labeled Traceability Lot Code.
5. Confirm the crop status becomes `Packed`.

Expected result: planting, initial care, issue, harvest, and pack/TLC actions generate the documented Cropchain records; daily care is summarized into harvest or loss evidence.

## 8. Close and anchor the season

1. As farm admin, open Admin → Season management.
2. Select `Close season`.
3. Review and sign the Cardano mainnet transaction.
4. Wait for Cardano acceptance and Blockfrost indexing.
5. If the season remains `closing`, select `Close season` again to reconcile the saved transaction. Do not intentionally create a duplicate transaction.

Expected result:

- The season record stream is frozen.
- A Merkle root is computed from the Cropchain records.
- Cardano metadata label `674` contains the root, season, farm, record count, and schema.
- The service reads the transaction back and marks the season anchored only after all fields match.

Capture:

- Close/anchor transaction hash and Cardanoscan link.
- Block number, slot, and chain timestamp.
- Merkle root and record count.
- Season ID and final status.
- Screenshot of the anchored season.
- Public validation report and raw JSON/archive URLs.

## 9. Independent validation

1. Open the public validation URL in a logged-out/incognito browser.
2. Confirm the reported season ID, Merkle root, record count, transaction hash, and Cardano metadata agree.
3. Open the Cardanoscan transaction independently.
4. Save the validation JSON/archive and calculate its SHA-256 checksum for the evidence repository.

Expected result: a third party can verify the season without project-team credentials.

## 10. Reviewer safety notes

- Never share a wallet seed phrase or private key.
- Verify the domain before signing.
- Read the transaction summary before approval.
- Use clearly labeled acceptance-test farm and season data.
- Redact personally identifying contact/location data from screenshots if necessary.

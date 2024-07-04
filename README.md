## Repro

Repro of https://github.com/foundry-rs/foundry/issues/5847

### Instructions

- forge install
- cd lib/optimism/packages/contracts-bedrock/

To bind with Ethers

- forge bind / forge bind --alloy

To bind with Alloy

- rm -rf forge-artifacts/bindings/
- forge bind --alloy

Change back to project root

- cd ../../../../
- cargo init --bin

Add `foundry-contracts = { path = "lib/optimism/packages/contracts-bedrock/forge-artifacts/bindings" }` to Cargo.toml

Check `src/main.rs`
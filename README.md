# `dfx-deploy-failure-example`

This repo is a small example of a bug I'm seeing when running `dfx deploy`.

The `store` canister is importing the `icp_ledger` canister via `import ic:ryjl3-tyaaa-aaaaa-aaaba-cai`.

When running `dfx deploy`, the command fails with the following error:

```
import error [M0009], file "~/dfx-deploy-failure-example/.dfx/local/canisters/idl/ryjl3-tyaaa-aaaaa-aaaba-cai.did" does not exist
```

## Running the project locally

```bash
# Starts the replica, running in the background
dfx start --background

# Pull, init, and deploy dependency canisters
dfx deps pull
dfx deps init
dfx deps deploy

# Deploys your canisters to the replica and generates your candid interface
dfx deploy
```

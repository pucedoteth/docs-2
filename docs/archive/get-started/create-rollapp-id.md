---
title: Create RollApp
slug: create-rollapp-id
---

To build our RollApp we must first register it with the Dymension Hub. Open a new terminal window and set the relevant environment variables for first creating a RollApp:

```bash
ROLLAPP_ID="local-rollapp"
```

Send a transaction to the Dymension Hub to create a namespace for the RollApp:

```bash
dymd tx rollapp create-rollapp "$ROLLAPP_ID" stamp1 "genesis-path/1" 3 100 '{"Addresses":[]}' \
  --from "$KEY_NAME" \
  --chain-id "$CHAIN_ID" \
  --keyring-backend test
```

The following flags are required as part of the tranaction:

-   `ROLLAPP_ID` is the unique identifier of the RollApp
-   `codeStamp` is the description of the genesis file location on the data layer
-   `genesisPath` is the description of the genesis file location on the data layer
-   `maxWithholdingBlocks` is the maximum number of blocks for an active sequencer to send a state update
-   `maxSequencers` is the maximum number of sequencers
-   `permissionedAddresses` is a bech32-encoded address list of the sequencers that are allowed to serve this ROLLAPP_ID
-   `--from` the name of the account that initializes the RollApp (in this example it is "user1")
-   `--chain-id` is the name of the chain (in this example it is "localnet")

Let's make sure the RollApp initialization worked:

```sh
dymd query rollapp list-rollapp
```

The previous query should result in:

```bash
rollapp:
  codeStamp: stamp1
  creator: <creator-address>
  genesisPath: genesis-path/1
  maxSequencers: "100"
  maxWithholdingBlocks: "3"
  permissionedAddresses:
    addresses: []
  rollappId: <RollApp ID>
  version: "0"
```

Contrary to general purpose smart contract blockchains, querying the state of the Dymension Hub blockchain allows users and applications to understand which RollApps exist in the ecosystem. This is what is often regarded as the embedded logic of RollApps in the Dymension Hub.

#### Let's add a sequencer to our RollApp...
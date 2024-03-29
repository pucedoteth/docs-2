---
title: "Troubleshooting"
slug: "troubleshooting"
---

Multiple issues can arise when running a node. This page provides possible solutions to some of the most common issues.

### Reset node

From time to time, you might encounter the need to fully reset your node due to issues like data corruption or configuration errors. This reset operation will eliminate all the data stored in ~/.dymension/data as well as the address book located in ~/.dymension/config/addrbook.json, reverting the node to its genesis state.

To execute a comprehensive reset of your dymd, use the following command:

```sh
  dymd tendermint unsafe-reset-all
```

Once this command is run successfully, it will generate the following log:

```
[ INF ] Removed existing address book file=/home/user/.dymension/config/addrbook.json
[ INF ] Removed all blockchain history dir=/home/user/.dymension/data
[ INF ] Reset private validator file to genesis state keyFile=/home/user/.dymension/config/priv_validator_key.json stateFile=/home/user/.dymension/data/priv_validator_state.json
```

This log indicates that the address book and all blockchain history have been removed, and the private validator file has been reset to the genesis state.

### Change Genesis

To change the genesis version, delete `~/.dymension/config/genesis.json`. Genesis files are provided in the [GitHub](https://github.com/dymensionxyz/testnets) for the appropriate networks.

### Reset personal data

You may be unable to use your node and its associated accounts after changing your personal data. Do not perform this action unless your node is disposable.

To change your personal data to a pristine state, delete both `~/.dymension/config/priv_validator_state.json` and `~/.dymension/config/node_key.json`.

### Node health

A healthy node will have the following files in place and populated:

-   Addressbook `~/.dymension/config/addrbook.json`
-   Genesis file `~/.dymension/config/genesis.json`
-   Validator state `~/.dymension/config/priv_validator_state.json`
-   Node key `~/.dymension/config/node_key.json`

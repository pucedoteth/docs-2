---
title: "dYmension Litepaper"
slug: "dymension-litepaper-index"
---

# dYmension Litepaper

## Home of the RollApps

Present day blockchains operate as shared bandwidth systems which impede the growth of decentralized applications. dYmension disaggregates resource consumption by introducing a multi-layer blockchain protocol with robust tooling for building and deploying permission-less application-specific rollups. dYmension is akin to a hub and factory for such applications, which are referred to as RollApps. In this document we examine the technological, economic and social aspects of the dYmension protocol. Furthermore, we present the grand vision for dYmension, the modular architecture of its design and a high level overview of dYmension’s prominent core concepts.

### Rollup Factory - RollApp Development Kit (RDK)

dYmension’s rollup factory takes its inspiration from the Cosmos ecosystem which introduced the successful Cosmos SDK. A RollApp instance on dYmension is an application-specific rollup, built using the dYmension RollApp Development Kit, termed RDK. The development kit is a pre-packaged set of generic modules for common functionalities such as creating accounts and token management. The RDK simplifies the process of deploying a RollApp on top of dYmension’s settlement layer.

### dYmension Settlement Layer

A Cosmos SDK Proof-of-Stake chain which utilizes the Tendermint Core state replication model for networking and consensus. Contrary to a monolithic blockchain, dYmension’s settlement layer, also referred to as a Hub, is specifically designed to provide an optimized service for rollups. As such, rollup servicing logic is enshrined within the settlement layer, resulting in a hub for native interoperability between RollApps.

### Inter-Rollup Communication (IRC)

IRC is an Inter-Blockchain Communication (IBC) based protocol which provides safe message transferring between dYmension RollApps. IRC leverages the common communication ground of all dYmension RollApps, the dYmension settlement hub.

### RollApp Virtual Machine (RVM)

dYmension introduces a novel dispute- resolution mechanism which simulates a RollApp execution environment within the settlement hub. The settlement hub spins up an RVM instance which is being fed with the exact context of a given transaction, resulting in a deterministic output. As such, dymension is capable of supporting various execution environments.

### Embedded Hub AMM

dYmension embeds a native Automated Market Maker (AMM) into the settlement hub to achieve shared liquidity on top of shared security. The AMM is designated for RollApp facilitation and is regarded as essential infrastructure for RollApps. The embedded AMM is the sole applicative logic on the settlement layer which is not restricted for RollApp usage only.

### Full PDF

Click [here for the full PDF of the dYmension Litepaper](https://litepaper.dymension.xyz/).
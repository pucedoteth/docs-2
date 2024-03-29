---
title: "Bridging"
slug: "bridging"
hide_table_of_contents: true
---

### Overview

Dymension's RDK builds upon the Cosmos SDK by adding new modules and modifying existing ones for ensuring RollApp compatibility with the Cosmos ecosystem. New modules are designed specifically for handling validator-less RollApp application logic. RollApps are capable of interacting with any IBC-enabled chain using the Dymension Hub and as such will be a part of the growing IBC ecosystem.

<div class="image-container-secondary">
    <img class="image--primary" src={require('../images/ibc-bridging.png').default} alt="dymint-overview" />
</div>

Dymension as a protocol is designed to facilitate the growth of the Cosmos and inter-chain ecosystem. By being natively IBC-enabled, the Dymension Hub facilitates trust-minimized message passing between RollApps, Cosmos zones, and further IBC-enabled ecosystems.

Unlike traditional Cosmos app-chains, RollApps delegate consensus to the Dymension Hub. The Dymension Hub thus acts as the decentralized source of truth and decides when a RollApp is in good standing. As such, the Dymension Hub intermediates transfers in and out of RollApps. By utilizing the existing IBC stack, RollApps are able to be compatible with the IBC-enabled ecosystem even without consensus.

### Escrow IBC

RollApp Sequencers produce and publish blocks optimistically (i.e. without active validation from Dymension Hub nodes). Thus, for bridging out the Dymension Hub enforces a dispute period for any network participant to submit a fraud proof againist the published state root. If no one submits a fraud proof, the state root is assumed to be valid for light clients.

For immediate IBC transfers, the Dymension protocol will implement a version of the [Escrow IBC](https://eibc.dymension.xyz/). This will facilitate market making opportunities for new participants and enable fast withdrawals for RollApp users. The specification of eIBC is in-progress and the Dymension core team welcomes all ecosystem participants in the [discussion](https://forum.dymension.xyz/t/escrow-ibc-eibc-a-new-protocol-for-fast-trust-minimized-bridging-between-optimistic-rollups/33) and development of the protocol.

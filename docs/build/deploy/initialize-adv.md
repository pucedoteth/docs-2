---
title: "Initialize"
slug: initialize-adv
---

Initializing the configuration files of the RollApp will create the necessary information to start a new RollApp. This is an advanced guide which will deploy a DA light client, Sequencer full node, and relayer node in seperate processes.

Initialize the RollApp with the following command:

```zsh
roller config init
```

An interactive guide will ask the following questions:

1. What is the RollApp name?
   <br />
   (i.e. ROLLAPP_9000_1 please note the suffix of `_9000_1` is required for EVM RollApps)
2. What is the name of the RollApp currency?
   <br />
   (i.e. aphoton, udym)
3. What is the amount of tokens to be minted on Genesis?
   <br />
   (i.e. 1000000)
4. What is the location data will be published to?
   <br />
   (i.e. Celestia, Avail)
5. What is the application environment?
   <br />
   (i.e. EVM, Go modules)

After completing the interactive questions, the Roller will have intialized the appropriate config files and should return addresses to fund:

```
💈 RollApp 'name' configuration files have been
   successfully generated on your local machine. Congratulations!

🔑 Addresses:

  Celestia         | celestia<ADDRESS>
  Dymension        | dym<ADDRESS>

🔔 Please fund these addresses to register and run the rollapp.
```

The following addresses must be funded prior to the following steps in this tutorial. Please fund the addresses at the following locations:

-   Celestia: Celestia discord channel for the Mocha network
-   Dymension: Dymension discord channel for the Froopyland network

Now that we've funded the wallets we can go ahead and register the RollApp!
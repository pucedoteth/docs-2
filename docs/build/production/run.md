---
title: "Run in Production"
slug: "run"
---

# Running in Production

This guide is designed to assist you in setting up the RollApp for production use. The focus will be on loading and starting the RollApp services individually. This approach enables independent logging and monitoring, giving you enhanced control and visibility over each component.

In addition, we'll be setting up a monitoring system using the well-known tools, Prometheus and Grafana. This will allow us to capture key metrics from our RollApp, set up alerts and understand the performance of our application over time.

By the end of this guide, you will have a production-grade local RollApp setup. Let's dive in!

## Starting the Rollapp Services

To load the rollapp services, use the following command:

```bash
$ roller services load
```

This command should return:

```
💈 Services 'sequencer', 'da-light-client' and 'relayer' been loaded successfully. To start them, use 'sudo systemctl start <service>'.
```

Next, start the services:

```bash
$ sudo systemctl start da-light-client
$ sudo systemctl start sequencer
$ sudo systemctl start relayer
```

Let's continue and set up the monitoring services...
---
title: "Postgres"
sidebar_position: 20
---

Snowplow supports loading data into Postgres.

In order to do this, you need to setup the [Postgres Loader](/docs/pipeline-components-and-applications/loaders-storage-targets/snowplow-postgres-loader/index.md), which can load enriched events from the enriched Pub/Sub topic, and load them into Postgres.
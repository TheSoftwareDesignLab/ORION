---
layout: page
title: SATCAT Module
description: Satellite Catalog module for Space Domain Awareness within Orion.
image:
  path: /assets/img/satcat-cover.png
---

## What is SATCAT?

The SATCAT module is a centralized satellite catalog system within Orion, designed to integrate and unify heterogeneous space object data from multiple open-source providers.

It enables tracking, characterization, and historical analysis of orbital objects using standardized identifiers such as NORAD ID.

---

## Key Features

- Multi-source data ingestion (Spacetrack, Celestrack, UCS, Satnogs, Satdb, DIsocsweb y nanosats)
- Automated normalization of heterogeneous orbital datasets
- Deduplication using NORAD ID
- Historical orbital state tracking
- REST API for query and integration
- PostgreSQL-backed structured catalog
- Real-time orbital propagation

---

## Architecture Overview

The SATCAT module is built using a layered architecture:

- Provider Layer: external data ingestion (APIs + scraping)
- Orchestration Layer: scheduling + ETL pipeline
- Persistence Layer: PostgreSQL database via SeaORM

### System Architecture Diagram
![Architecture](/assets/img/satcat-architecture.png)

This design ensures modularity, scalability, and independence between components.

---

## Results

*Media*

### Demo Video
<video controls src="/assets/video/satcat-demo.mp4"></video>
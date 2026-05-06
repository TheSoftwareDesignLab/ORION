---
layout: page
title: ORION
---

## What is ORION

ORION is a modular Space Domain Awareness (SDA) platform designed to support the integration, processing, and analysis of heterogeneous orbital data from multiple open-source repositories.

The system is developed to reduce manual workload in satellite catalog maintenance and enable automated decision-support capabilities for space operations through a unified data architecture.

---
## SDA Modules within ORION

ORION is composed of multiple functional modules:

- **SATCAT**: Satellite catalog and orbital object management
- **GNSS**: Satellite visibility and navigation analysis
- **Threat Assessment**: Conjunctions, anomalies, and risk detection
- **Space Weather**: Solar activity and environmental monitoring
- **Launch Planning**: Pre-launch environmental and risk analysis

Each module operates independently but shares a unified data backbone.

---

## Architecture Overview

ORION follows a modular microservices architecture composed of four main layers. Each layer is responsible for a specific stage of the data lifecycle, from ingestion to user interaction.

| Layer | Responsibility | Key Components | Description |
|------|---------------|----------------|-------------|
| Provider Layer | Data ingestion | Space-Track, CelesTrak, SatNOGS, DISCOSWeb, UCS DB | Interfaces with external sources and retrieves heterogeneous orbital data |
| Orchestration Layer | ETL processing | Scheduler, Normalizer, Deduplicator, Fusion Engine | Standardizes and consolidates data using NORAD ID and unified schemas |
| Persistence Layer | Data storage | PostgreSQL + SeaORM | Ensures structured storage, relational integrity, and historical tracking |
| Interface Layer | User interaction | React SPA + Axum API + SSE | Provides visualization, APIs, and real-time updates |

### System Architecture Diagram
![Architecture](/assets/img/orion-architecture.png)

---

## System Design Principles

- **Modularity**: each SDA function is an independent service
- **Transparency**: fully open-source data ingestion pipeline
- **Scalability**: microservices-based architecture
- **Auditability**: traceable data processing workflow
- **Autonomy**: reduced dependency on commercial SDA platforms

---
### Project Team

- Juan Camilo Beltrán Garnica (Universidad de los Andes) jc.beltrang1@uniandes.edu.co 
- Danna Lucia Castillo Palacios (Universidad de los Andes) d.castillop@uniandes.edu.co 
- David Camilo Ocaña Orbes (Fuerza Aeroespacial Colombiana) david.ocana@fac.mil.co 
- Mateo Cubides Galeano (Fuerza Aeroespacial Colombiana) mateo.cubides@fac.mil.co 
- Mario Linares Vásquez (Universidad de los Andes) m.linaresv@uniandes.edu.cov

This project is developed in collaboration between:

- **Fuerza Aeroespacial Colombiana (FAC)**
- **Universidad de los Andes**

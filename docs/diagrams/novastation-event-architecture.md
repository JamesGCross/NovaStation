# NovaStation Event Architecture (v1)

This diagram represents the logical, event-driven architecture of the NovaStation system.

## Overview

NovaStation is designed as a modular, event-driven system with a centralized decision engine (**Katsumi**) and distributed domain services.

Core components:

- **Katsumi** – decision routing, intent parsing, orchestration  
- **Event Bus** – central communication layer (MQTT / Mosquitto)  
- **Domain Services**  
  - **Lain** – music systems  
  - **Yomiko** – media systems & archives  
  - **Nami** – security authority  
  - **Misaki** – diagnostics & system visibility  

---

## Architecture Flow

User interaction flows through the system as follows:

```
Users → Interfaces → Katsumi → Event Bus → Services
```

Services execute actions and publish state back into the system:

```
Services → Event Bus → Katsumi (and other consumers)
```

---

## Core Principle

All communication is event-driven and flows through the Event Bus.

- No service communicates directly with another  
- No service communicates directly with Katsumi  
- All commands and feedback are published as events  

---

## Event Types

The system distinguishes between several types of events:

- **Command Events** – instructions issued by Katsumi  
- **State Events** – current status of services  
- **Telemetry Events** – system metrics and diagnostics  
- **Alert Events** – security or system warnings  
- **Assistant Events** – higher-level orchestration signals  

---

## Diagram Conventions

- **Downward arrows (↓)** represent command flow  
- **Upward arrows (↑)** represent state / telemetry flow  
- All arrows connect through the Event Bus (no direct coupling)

---

## Notes

This diagram represents the **logical architecture only**.

It does not include:
- infrastructure / deployment details  
- hardware topology  
- networking or VLAN configuration  

Those will be documented separately.

---

## Version

- **v1** – Initial event-driven architecture definition

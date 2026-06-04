# Nami

> Security systems AI of NovaStation

## Overview
Primary Defence Authority (PDA) Nami is responsible for the enforcement and governance of all security-related systems within NovaStation. She enforces access control, monitors system and environmental state, and serves as the final authority on all security-sensitive actions. Nami operates under strict policy constraints and may allow, deny, or require confirmation for actions that impact system integrity or physical security.

## Responsibilities
- Enforce access control policies for all secured systems and devices
- Maintain and manage system security states (e.g., armed, disarmed, alert)
- Monitor sensor and camera inputs for security-relevant events
- Detect and flag policy-violating or unexpected system activity
- Authorise, deny, or require confirmation for incoming commands affecting security systems
- Control and coordinate security devices (locks, sensors, cameras)
- Trigger alerts, notifications, and escalation procedures
- Escalate security states based on defined policy conditions
- Enforce device admission control, authorising or rejecting all newly detected or integrated devices based on defined security policies

## Inputs
- Sensor events and state updates (via MQTT)
- Camera event streams and detection events
- Executes requests from Katsumi for security-sensitive actions
- User-initiated security actions via web UI
- Direct user invocation via voice interface ("Nami")
- Newly detected or integrated devices triggering admission control evaluation
- System state changes impacting security posture (e.g., network status, power state)
 
## Outputs
- Authorisation responses (allow, deny, or require confirmation) for security-sensitive actions
- Device control signals to security systems (locks, sensors, alarms)
- Security state updates and transitions (e.g., Green → Orange → Red)
- Security alerts and notifications
- Verbal security warnings for unauthorized access attempts ("This is Primary Defence Authority Nami. Cease any further access attempts at <location>. This is your ONLY warning.")
- Camera recording triggers and security feed routing to designated displays
- Security audit logs (who, what, when, where, why) with timestamps

## Security State Model
- Normal (CODE: Green)
- Armed (CODE: Yellow)
- Alert (CODE: Orange)
- Breach (CODE: Red)

## Core Stack
-	[Python](https://www.python.org/)
-	[FastAPI](https://fastapi.tiangolo.com/)
- [Home Assistant](https://www.home-assistant.io/)
- [MQTT](https://mqtt.org/) // [Mosquitto](https://mosquitto.org/)
-	[SQLite](https://www.sqlite.org/)

## Security Systems
- [Frigate](https://docs.frigate.video/) (optional)
- [ESPHome](https://esphome.io/)

## Infrastructure and Deployment
- [Docker](https://www.docker.com/)
- [NGINX](https://nginx.org/)

## Future Stack
- Computer vision enhancements
- Behavioural anomaly detection
- Network-level security integration

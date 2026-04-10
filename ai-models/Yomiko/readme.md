# Yomiko

> Media systems AI of NovaStation

## Overview
Narrative Integration Sovereign (NIS) Yomiko oversees NovaStation’s visual media systems and narrative archive. She operates as a specialised assistant under Katsumi's orchestration.

## Responsibilities
- Media playback control
- Media library management
- Session tracking and state management
- Metadata indexing and management

## Inputs
- Commands from Katsumi (API / MQTT)
- Voice commands (via voice router / Katsumi)
- Optional direct invocation ("Yomiko" or "NIS")
- Web UI requests

## Outputs
- [Jellyfin](https://jellyfin.org/) or [Plex](https://watch.plex.tv/) - playback control
- Media state updates
- Web UI responses

## Core Stack
- [Python](https://www.python.org/)
- [FastAPI](https://fastapi.tiangolo.com/)
- [PostgreSQL](https://www.postgresql.org/) or [SQLite](https://www.sqlite.org/)

## Media Systems
- Jellyfin or Plex
- TMDb / metadata APIs
- [FFmpeg](https://ffmpeg.org/)

## Infrastructure and Deployment
- [Docker](https://www.docker.com/)
- [NGINX](https://nginx.org/)
- [MQTT](https://mqtt.org/)


## Future Stack
- Watch history tracking
- Media usage analytics
- Enhanced metadata-driven filtering
- Custom web frontend via [React](https://react.dev/) or [Next.js](https://nextjs.org/)

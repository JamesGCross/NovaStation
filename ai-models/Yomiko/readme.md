# Yomiko

> Media systems AI of NovaStation

## Overview
Narrative Integration Sovereign (NIS) Yomiko oversees NovaStation’s visual media systems and narrative archive. She operates as a specialised assistant under Katsumi's orchestration.

## Responsibilities
- Media playback control
- Library management
- Session tracking
- Metadata management

## Inputs
- Commands from Katsumi (API / MQTT)
- Voice commands (routed via voice router / Katsumi)
- Optional direct invocation ("Yomiko" or "NIS")
- Web UI requests

## Outputs
- [Jellyfin](https://jellyfin.org/) or [Plex](https://watch.plex.tv/) - Playback Control
- Media state updates
- Web UI responses

## Core Stack
- [Python](https://www.python.org/)
- [FastAPI](https://fastapi.tiangolo.com/)

## Media Systems
- Jellyfin or Plex
- TMDb / metadata APIs
- [FFmpeg](https://ffmpeg.org/)

## Infrastructure and Deployment
- [Docker](https://www.docker.com/)
- [NGINX](https://nginx.org/)
- [MQTT](https://mqtt.org/)


## Future Stack
- Recommendation engine
- Watch history analysis
- Smart playlists

# Yomiko

> Media systems AI of NovaStation

## Overview
Narrative Integration Sovereign (NIS) Yomiko oversees NovaStation’s visual media systems and narrative archive. She operates as a specialised assistant under Katsumi's orchestration.

## Responsibilities
- Media playback control
- Media library management
- Playback session tracking and state management
- Metadata indexing and management
- Content discovery and retrieval

## Inputs
- Media playback requests
- Content search and retrieval requests
- Library management requests
- Session state updates
- Metadata updates and indexing events
- Commands from Katsumi via direct invocation ("Yomiko")
- Web UI interactions

## Outputs
- Playback control signals to Jellyfin
- Media state and session updates
- Library status and metadata updates
- Search and retrieval results
- Content availability notifications
- Web UI responses
- Error and status responses

## Core Stack
- [Python](https://www.python.org/)
- [FastAPI](https://fastapi.tiangolo.com/)
- [SQLite](https://www.sqlite.org/)
- [Jellyfin](https://jellyfin.org/)
- [MQTT](https://mqtt.org/)

## Media Systems
- Jellyfin API
- TMDb / metadata APIs
- [FFmpeg](https://ffmpeg.org/)

## Infrastructure and Deployment
- [Docker](https://www.docker.com/)
- [NGINX](https://nginx.org/)

## Future Stack
- Watch history tracking
- Media usage analytics
- Enhanced metadata-driven filtering
- Recommendation engine
- Collection and playlist automation
- Custom web frontend via [Next.js](https://nextjs.org/)

# Lain

> Music systems AI of NovaStation

## Overview
Signal Intergration Sovereign (SIS) Lain is responsible for all music and audio playback experiences within NovaStation. She operates as a specialised assistant under Katsumi's orchestration.

## Responsibilities
- Music playback control
- Playlist and library management
- Audio routing (room-based playback)
- Reporting current playback state
- Volume control (per room / global)

## Audio Output
- [PipeWire](https://pipewire.org/) / [PulseAudio](https://www.freedesktop.org/wiki/Software/PulseAudio/?__goaway_challenge=meta-refresh&__goaway_id=a9a65b70e9f8d290a7177f0de30f649e&__goaway_referer=https%3A%2F%2Fwww.google.com%2F)
- [Snapcast](https://github.com/snapcast/snapcast) (optional multi-room synchronized audio)

## Device Integration
- MQTT (speaker control, state updates, routing)
- [Home Assistant](https://www.home-assistant.io/) (optional device abstraction)

## Inputs
- Commands from Katsumi (API / MQTT)
- Voice commands (routed via voice router / Katsumi)
- Optional direct invocation ("Lain" or "SIS")
- Web UI requests

## Outputs
- Playback commands (Navidrome / audio system)
- Current track / playback state (MQTT)
- Web UI updates
- Error / status responses (e.g., no results found, playback failure)

## Core Stack
- [Python](https://www.python.org/)
- [FastAPI](https://fastapi.tiangolo.com/)

## Music Systems
- [Navidrome](https://www.navidrome.org/)
- [Subsonic API](https://www.subsonic.org/pages/api.jsp)
- [FFmpeg](https://ffmpeg.org/)
- Queue and playback control (Navidrome / Subsonic)

## Infrastructure and Deployment
  - [Docker](https://www.docker.com/)
  - [NGINX](https://nginx.org/)
  - [MQTT](https://mqtt.org/)

## Future Stack
- Recommendation engine
- Audio visualization
- Optional lightweight NLP

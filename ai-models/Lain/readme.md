# Lain

> Music systems AI of NovaStation

## Overview
Signal Integration Sovereign (SIS) Lain is responsible for all music and audio playback experiences within NovaStation. She operates as a specialised assistant under Katsumi's orchestration.

## Responsibilities
- Music playback control
- Playlist and library management
- Audio routing for room-based playback
- Volume control for individual rooms and global playback
- Reporting current playback state
- Managing playback queues and music sessions

## Inputs
- Commands from Katsumi (API / MQTT)
- Voice commands routed through Katsumi
- Web UI requests
- Room or zone playback requests
- Music search and playlist requests

## Outputs
- Playback control signals to Navidrome and room audio systems
- Current track and playback state updates
- Room / zone playback status
- Web UI updates
- Error and status responses

## Core Stack
- [Python](https://www.python.org/)
- [FastAPI](https://fastapi.tiangolo.com/)
- [Navidrome](https://www.navidrome.org/)
- [MQTT](https://mqtt.org/) // [Mosquitto](https://mosquitto.org/)
- [Subsonic API](https://www.subsonic.org/pages/api.jsp)
- [SQLite](https://sqlite.org/)

## Music Systems
- [FFmpeg](https://ffmpeg.org/)
- [PipeWire](https://pipewire.org/) // [PulseAudio](https://www.freedesktop.org/wiki/Software/PulseAudio/?__goaway_challenge=meta-refresh&__goaway_id=a9a65b70e9f8d290a7177f0de30f649e&__goaway_referer=https%3A%2F%2Fwww.google.com%2F)
- [Snapcast](https://github.com/snapcast/snapcast) (optional multi-room synchronised audio)
- Queue and playback control

## Infrastructure and Deployment
- [Docker](https://www.docker.com/)
- [NGINX](https://nginx.org/)
  
## Future Stack
- Recommendation engine
- Audio visualisation
- Smart playlist generation
- Listening history and preference modelling
- Room-aware playback automation

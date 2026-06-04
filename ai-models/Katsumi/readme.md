# Katsumi
> Core orchestration AI of NovaStation

## Overview
Katsumi is the Commander of the NovaStation Complex and the central AI Assistant. She acts as the central orchestration layer, coordinating all subordinate assistants.

## Responsibilities
- Voice command processing
- Task orchestration
- Cross-assistant coordination
- Contextual memory and conversation continuity
- Intent recognition and routing
- Context management
- Assistant delegation
- User interaction management

## Inputs
- Voice commands (STT pipeline)
- Web UI requests
- MQTT messages
- API calls
- Responses from subordinate assistants
- System status events
- Security authorisation responses from Nami
- Operational health reports from Misaki

## Outputs
- Assistant-to-assistant commands (MQTT / API)
- Spoken responses (TTS)
- System actions (Home Assistant)
- Web UI responses
- Event bus publications
- Assistant routing decisions
  
## Core Stack:
  -	[Python](https://www.python.org/)
    - Main language for all of NovaStation, backend logic, orchestration, assistant behaviour, API pulls, et al
  -	[FastAPI](https://fastapi.tiangolo.com/)
    - This is used for Katsumi’s internal API and service endpoints
  -	[Pydantic](https://docs.pydantic.dev/latest/)
    - Utilised for request/response validation and structured models
  -	[SQLite](https://www.sqlite.org/)
     - Memory, preferences, structures states, and logs

## AI / Language / Voice:
  - LLM Backend
    - Primary: [Ollama](https://ollama.com/)
    - Alternative: [Llama.cpp](https://llama-cpp.com/) for lower level control
	  - OPTIONAL: remote model APIs if needed
	- NLP and Intent Recognition
	  - [spaCy](https://spacy.io/); [Rasa](https://rasa.com/)
	- Speech-to-Text
	    - [Whisper](https://openai.com/index/whisper/); [fasterWhisper](https://pypi.org/project/faster-whisper/0.3.0/); [Vosk](https://alphacephei.com/vosk/)
	- Text-to-Speech
      - [Piper](https://github.com/OHF-Voice/piper1-gpl) [Piper 1](https://github.com/rhasspy) [Piper 2](https://www.xda-developers.com/home-assistant-piper-streaming-audio-support/); [Coqui-AI](https://github.com/coqui-ai/tts); [Azure TTS](https://azure.microsoft.com/en-us/products/ai-foundry/tools/speech); [ElevenLabs](https://elevenlabs.io/)
    - Wake Word
      - [Porcupine](https://picovoice.ai/platform/porcupine/); [OpenWakeWord](https://openwakeword.com/)

## Home Automation and Coordination:
- [Home Assistant](https://www.home-assistant.io/)
- [MQTT](https://mqtt.org/)
- [Mosquitto](https://mosquitto.org/)
- [ESPHome](https://esphome.io/) for custom sensors/mics/switches

## Infrastructure and Deployment:
- [Void Linux](https://voidlinux.org/)
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
- [NGINX](https://nginx.org/)

## Future Stack:
- Long-term memory and semantic retrieval
- Advanced orchestration workflows
- Emotional context modelling
- Multi-user preference management
- Autonomous task planning
- Vector Database: [Qdrant](https://qdrant.tech/)
- Orchestration Layer: [LangChain](https://www.langchain.com/)
- Emotional Analysis // Intelligence: [BERT](https://huggingface.co/bhadresh-savani/bert-base-uncased-emotion); [RoBERTa](https://huggingface.co/SamLowe/roberta-base-go_emotions)
- [Redis](https://redis.io/)
  - Optional caching, queuing, or temporary context

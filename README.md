# AI Call Bot

An **AI-powered Call Bot** that integrates real-time telephony with speech-to-text, text-to-speech, conversational AI, and **automatic appointment booking** in Google Calendar.  

The system answers calls, transcribes speech, generates AI-driven responses, and speaks them back to the caller. If the caller requests an appointment, the bot automatically checks availability and schedules it in Google Calendar via the Google API.  

> ⚠️ Due to security and permission restrictions (Google service account & OAuth credentials), the complete codebase is **kept private**. This repository documents the project, its design, and its workflows.

---

## Table of Contents
- [About the Project](#about-the-project)  
- [Features](#features)  
- [Technology Stack](#technology-stack)  
- [Getting Started](#getting-started)  
- [Project Flow](#project-flow)  
- [Future Improvements](#future-improvements)  
- [License](#license)  
- [Contact](#contact)  

---

## About the Project
The **AI Call Bot** is a telephony + AI system that demonstrates end-to-end automation of phone conversations and scheduling:  

- Handles inbound calls via **Asterisk PBX (Dockerized)**  
- Uses **speech-to-text** (Whisper / Vosk) to transcribe live caller audio  
- Sends transcripts to an **AI model (LLM)** for conversational responses  
- Converts AI replies to **speech (TTS)** and plays them back to the caller  
- **Automatically books appointments in Google Calendar** when requested  
- Logs all transcripts and scheduling actions  

---

## Features
- **Inbound Call Handling**: Routes calls via Asterisk SIP endpoints  
- **Real-Time Transcription**: Whisper/Vosk for accurate STT  
- **Conversational AI**: LLM-powered responses with context awareness  
- **TTS Playback**: AI replies converted to natural-sounding audio  
- **Calendar Integration**: Automatically creates Google Calendar events  
- **Logging & Audit**: Tracks conversations and appointments  
- **Secure by Design**: Sensitive credentials excluded; private repo maintained  

---

## Technology Stack

### Telephony
- Asterisk PBX (Dockerized)  
- PJSIP for SIP endpoints  

### Speech & AI
- Whisper / Vosk (STT)  
- ElevenLabs / Google / Azure TTS (TTS)  
- LLMs (OpenAI / Hugging Face)  

### Backend
- Python (bot orchestration, API integration)  
- Google Calendar API (appointment booking)  

### Tools & Libraries
- Flask / FastAPI (optional APIs)  
- ffmpeg, pyaudio  
- Google API Python Client  

---

## Getting Started
> ⚠️ Full codebase is **private** because it contains sensitive credentials and Google OAuth permissions.  

If you wish to recreate a similar setup:  
1. Setup Asterisk in Docker  
2. Use Whisper/Vosk for STT  
3. Connect LLM for conversational flow  
4. Use Google Calendar API with OAuth2 for booking  
5. Exclude all credentials from public repos  

---

## Project Flow

### Call Flow
1. Caller dials in → Asterisk routes audio  
2. Audio → STT → text transcript  
3. Transcript → AI model → response  
4. Response → TTS → playback to caller  
5. If appointment requested → Google Calendar API event created  
6. Confirmation spoken back to caller  

### Calendar Flow
- Bot checks availability via Google Calendar API  
- Creates event with caller’s details  
- Sends calendar invite & logs confirmation  

---

## Future Improvements
- Multi-user calendar support  
- Outbound call support (reminders, confirmations)  
- Multi-language STT/TTS  
- Real-time streaming with WebRTC  
- Web dashboard for logs and analytics  

---

## License
Distributed under the MIT License. See `LICENSE` for details.  

---

## Contact
**Author:** Uma Pratyusha Putcha  
- Email: umaputcha9@gmail.com  
- GitHub: [github.com/pratyusha56](https://github.com/pratyusha56)  
- LinkedIn: [linkedin.com/in/uma-pratyusha-putcha-1b44231b6](https://www.linkedin.com/in/uma-pratyusha-putcha-1b44231b6)  

---

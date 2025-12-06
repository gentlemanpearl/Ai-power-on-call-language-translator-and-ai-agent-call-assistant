# Ai-power-on-call-language-translator-and-ai-agent-call-assistant
Breaking language barriers in telecom with AI. 🌍🎙️ A real-time voice translation system featuring bi-directional translation, voice cloning (Coqui TTS), and Agentic AI (GPT-4) for live insights and automated WhatsApp summaries.

# 📞 AI-Powered Real-Time Voice Translator & Intelligent Assistant

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![FastAPI](https://img.shields.io/badge/FastAPI-0.68+-green.svg)
![OpenAI](https://img.shields.io/badge/AI-Agentic-orange.svg)
![Coqui TTS](https://img.shields.io/badge/Voice-Cloning-purple.svg)

**Revolutionizing cross-language communication with Voice Cloning and Agentic AI.**

## 🚀 Overview
This project is a modular AI system designed for the Telecommunications industry. It enables two speakers of different languages to communicate seamlessly in real-time. Unlike standard translators, this system **clones the speaker's voice** to maintain authenticity and uses a parallel **AI Agent** to analyze the conversation for action items and sentiment.

## ✨ Key Features
* **🗣️ The Ear (STT):** High-accuracy real-time speech recognition using `Vosk` (Offline/Privacy-focused).
* **🧠 The Brain (Agentic AI):** A background `GPT-4` agent that listens, extracts tasks, detects mood, and generates summaries without blocking the call flow.
* **🎙️ The Voice (Cloning):** Uses `Coqui TTS` to translate speech while preserving the original speaker's timbre and tone.
* **⚡ Low Latency:** Built on `FastAPI WebSockets` and `asyncio` for non-blocking, bidirectional streaming.
* **📱 Instant Delivery:** Automatically formats and sends "Meeting Minutes" to WhatsApp immediately after the call.

## 🛠️ Architecture
The system follows a "Forked Pipeline" architecture:
1.  **Input:** WebSocket stream captures raw audio.
2.  **Path A (Voice):** STT -> Translation -> Voice Cloning -> Audio Output.
3.  **Path B (Intelligence):** STT -> Buffer -> GPT-4 Analysis -> Action Item Extraction.

## 📦 Installation

```bash
# Clone the repo
git clone [https://github.com/yourusername/telecom-ai-assistant.git](https://github.com/yourusername/telecom-ai-assistant.git)

# Install dependencies
pip install -r requirements.txt

# Run the server
python main.py

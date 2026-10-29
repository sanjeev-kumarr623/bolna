# Voice Agents Platform

**End-to-end open-source voice agents platform**: Quickly build voice-first conversational assistants through a simple configuration JSON.

---

## Introduction

This is an end-to-end, open-source, production-ready framework for quickly building LLM-based voice-driven conversational applications.

## What is this repository?

This repository contains the entire orchestration platform to build voice AI applications. It technically orchestrates voice conversations using a combination of different ASR, LLM, and TTS providers and models over websockets.

## Components

This platform helps you create AI voice agents which can be instructed to perform tasks using:

1. The core orchestration platform (this repository)
2. Custom hosted APIs built on top of this orchestration platform
3. No-code UI dashboard playground utilizing the orchestration APIs

---

## Supported Providers and Models

1. **Telephony Providers**: Twilio, Plivo, and other extensible telephony channels.
2. **ASR (Speech-to-Text)**: Deepgram, Azure, and other transcription backends.
3. **LLMs**: OpenAI, DeepSeek, Llama, Cohere, Mistral, and any LiteLLM-compatible model.
4. **TTS (Text-to-Speech)**: AWS Polly, ElevenLabs, Deepgram, OpenAI, Azure, Cartesia, and Smallest.

---

## Local Setup & Quick Start

A basic local setup includes usage of Twilio or Plivo for telephony. We have dockerized the setup in `local_setup/`. Copy the `.env.sample` file to create your own `.env` file and populate your provider API keys.

The setup consists of four primary containers:
1. **Telephony web server** (Twilio or Plivo integration)
2. **Core application server** (for creating and handling agents)
3. **`ngrok`** (for tunneling webhook traffic)
4. **`redis`** (for persisting agents & prompt data)

### Quick Start with Docker

```bash
cd local_setup
chmod +x start.sh
./start.sh

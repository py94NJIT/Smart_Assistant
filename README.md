# Raspberry Pi Smart Assistant
This project creates a basic voice-controlled smart assistant running on a Raspberry Pi. It uses Python to listen for your commands and respond, bringing simple voice interaction to your DIY projects.

## Features
Voice Recognition: Understands spoken commands using Google's Speech Recognition API.

Text-to-Speech (TTS): Responds to you with a synthesized voice.

Basic Command Processing: Currently supports simple greetings and a quit command.

## Installation
Prerequisites
Raspberry Pi (any model should work, but a newer one will provide better performance).

Microphone (USB microphone recommended).

Speakers or headphones.

Python 3 (usually pre-installed on Raspberry Pi OS).

## How it Works
The core of the assistant is built around a few key functions:

speak(text): Takes text as input and uses pyttsx3 to convert it into speech.

listen(): Captures audio from your microphone, adjusts for ambient noise, and then sends it to Google's Speech Recognition service to convert the speech into text. It includes error handling for when speech isn't recognized or the service is unreachable.

process_command(command): This is where the assistant's "intelligence" resides. It checks the recognized text for keywords and triggers appropriate responses.

The main loop continuously listens for commands and processes them until the "quit" command is given.

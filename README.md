# Modern AI Chatbot with SmolLM2

## Overview

This project implements a conversational AI chatbot using **SmolLM2-360M-Instruct**, a lightweight instruction-tuned causal language model developed by Hugging Face.

Built with Python, PyTorch, and Hugging Face Transformers, the chatbot uses structured conversation messages and model-specific chat templates to generate context-aware responses.

This project was developed as part of my learning journey in Large Language Models (LLMs) and Natural Language Processing (NLP), following IBM's chatbot development coursework.

## Features

- Pretrained causal language model using SmolLM2-360M-Instruct
- Structured conversation history using system, user, and assistant roles
- Hugging Face chat templates for model-specific prompt formatting
- Token-by-token text generation
- Configurable generation parameters, including temperature, top-p sampling, and repetition penalty
- Context management to retain recent conversation messages
- Terminal-based conversational interface
- CPU-based inference using PyTorch

## Technologies

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Hugging Face Transformers | Model and tokenizer loading |
| SmolLM2-360M-Instruct | Conversational language model |
| PyTorch | Model inference |
| Git and GitHub | Version control and project hosting |

## Model

**Model:** [HuggingFaceTB/SmolLM2-360M-Instruct](https://huggingface.co/HuggingFaceTB/SmolLM2-360M-Instruct)

SmolLM2 is a lightweight family of language models. The 360M Instruct variant is fine-tuned to follow instructions and perform conversational tasks.

## How It Works

1. Load the pretrained model and its tokenizer.
2. Initialize the conversation with a system instruction.
3. Collect user messages and store them in a structured conversation history.
4. Apply the model's chat template to format the conversation.
5. Generate a response using the causal language model.
6. Decode the generated tokens into readable text.
7. Append the assistant's response to the conversation history.

## Installation

Clone the repository:

```bash
git clone https://github.com/Betty401/ai-chatbot-smollm2.git
cd ai-chatbot-smollm2
```

Create and activate a virtual environment:

**Windows PowerShell:**

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

## Usage

Run the chatbot:

```bash
python chatbot_llm.py
```

The model will be downloaded automatically the first time it is loaded.

Type a message to start a conversation. Enter `exit` to terminate the chatbot.

## Project Structure

```text
ai-chatbot-smollm2/
│
├── chatbot_llm.py
├── requirements.txt
├── README.md
├── .gitignore
└── .venv/              # Local environment; excluded from Git
```

## Learning Objectives

This project explores:

- The difference between encoder-decoder and causal language models
- Tokenization and pretrained language models
- Structured conversational messages and role-based history
- Hugging Face chat templates
- Autoregressive text generation
- Sampling strategies and generation parameters
- Context management in conversational AI

## Limitations

This project uses a relatively small language model and is intended for educational purposes. Response quality, factual accuracy, and conversational memory are limited by the model's capabilities.

It is a terminal-based demonstration and does not provide a production-ready chatbot interface.

## Acknowledgments

Developed as part of IBM's learning materials on building conversational AI systems, using Hugging Face Transformers and the SmolLM2 model.
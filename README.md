# Adaptive Memory v3.1 for OpenWebUI

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![OpenWebUI Plugin](https://img.shields.io/badge/OpenWebUI-Plugin-green.svg)](https://github.com/open-webui/open-webui)

> A sophisticated plugin that provides persistent, personalized memory capabilities for LLMs within OpenWebUI.

Adaptive Memory automatically learns facts, preferences, and goals from your AI conversations and intelligently injects relevant memories into future prompts—creating a more natural and personalized experience.

---

## ✨ Key Features

- **Auto-Learning** — Automatically extracts facts (e.g., "I live in Paris"), preferences (e.g., "I prefer Python"), and goals from conversations
- **Smart Retrieval** — Vector-based similarity for efficient, contextually relevant memory retrieval
- **Deduplication** — Multi-layered semantic and text-based similarity to prevent duplicate memories
- **Memory Banks** — Categorize memories into **General**, **Personal**, **Work**, etc. for focused retrieval
- **Auto-Summarization** — Periodically condenses older memories to save space and reduce clutter
- **Memory Confidence Scoring** — Filters low-quality memories based on configurable thresholds
- **Flexible Providers** — Supports both Ollama and OpenAI-compatible APIs for LLM and embeddings
- **Health Monitoring** — Prometheus metrics and health endpoints for observability

---

## 🚀 Quick Start

1. **Install the Plugin:** Copy `adaptive_memory_v3.1.py` to your OpenWebUI plugins folder
2. **Enable the Plugin:** Go to **Workspace → Tools → Adaptive Memory** and toggle valid valves
3. **Basic Configuration:**
   - **Embedding Provider**: Choose `local` (free, runs on your server) or `openai_compatible` (external API)
   - **LLM Provider**: Choose `ollama` (default) or `openai_compatible`
4. **Start Chatting:** The AI will now start remembering key details about you!

---

## ⚙️ Configuration Guide ("Valves")

| Setting | Description |
|---------|-------------|
| **Embedding Provider** | `local` or `openai_compatible` |
| **LLM Provider** | `ollama` or `openai_compatible` |
| **Minimum Confidence** | How certain the AI must be to save a memory (0.0 - 1.0) |
| **Duplicate Threshold** | How strictly duplicates are detected |

Advanced settings like auto-summarization and custom memory banks generally don't need changing.

---

## 💬 Chat Commands

| Command | Description |
|---------|-------------|
| `/memory status` | Check if memory is active |
| `/memory list` | View all stored memories |
| `/memory forget [id]` | Delete a specific memory |
| `/memory list_banks` | See available memory banks |
| `/memory assist` | Get help with memory features |

---

## 🔧 Troubleshooting

| Issue | Solution |
|-------|----------|
| **"No memories found"** | Chat more naturally about yourself. Ensure `Minimum Confidence` isn't set too high (default 0.75 is good) |
| **Errors** | Check OpenWebUI logs. Verify your LLM and Embedding provider URLs are correct |

---

## 📊 API Endpoints

- `GET /adaptive-memory/health` — Health check
- `GET /adaptive-memory/metrics` — Prometheus metrics

---

## 🙏 Credits

Based on the original work by [gramanoid](https://github.com/gramanoid/owui-adaptive-memory).

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

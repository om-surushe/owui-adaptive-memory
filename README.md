# Adaptive Memory v3.1 for OpenWebUI

Adaptive Memory provides persistent, personalized long-term memory for your AI conversations. It automatically learns facts, preferences, and goals from your chats and injects them into future conversations where relevant.

## Quick Start

1.  **Enable the Plugin:** Go to **Workspace > Tools > Adaptive Memory** and toggle valid valves.
2.  **Basic Configuration:**
    *   **Embedding Provider**: Choose `local` (free, runs on your server) or `openai_compatible` (external API).
    *   **LLM Provider**: Choose `ollama` (default) or `openai_compatible`.
3.  **Start Chatting:** The AI will now start remembering key details about you!

## Key Features

*   **Auto-Learning:** Automatically extracts facts (e.g., "I live in Paris") and preferences (e.g., "I prefer Python").
*   **Smart Retrieval:** Finds only relevant memories for the current conversation.
*   **Deduplication:** Prevents duplicate memories using advanced semantic checking.
*   **Memory Banks:** Categorizes memories into **General**, **Personal**, **Work**, etc.
    *   *Usage:* The system automatically assigns banks. You can also manually assign banks using commands if needed.
*   **Auto-Summarization:** Periodically condenses older memories to save space.

## Configuration Guide ("Valves")

*   **Basic Configuration**: Set your Embedding and LLM providers.
*   **Memory Quality**:
    *   `Minimum Confidence`: Control how certain the AI must be to save a memory (0.0 - 1.0). Higher = stricter.
    *   `Duplicate Threshold`: Control how strictly duplicates are detected.
*   **Advanced**: Settings like auto-summarization and custom memory banks generally don't need changing.

## Chat Commands

*   `/memory status` - Check if memory is active.
*   `/memory list` - View all stored memories.
*   `/memory forget [id]` - Delete a specific memory.
*   `/memory list_banks` - See available memory banks.
*   `/memory assist` - Get help with memory features.

## Troubleshooting

*   **"No memories found"**: Try chatting more naturally about yourself. Ensure `Minimum Confidence` isn't set too high (default 0.75 is good).
*   **Errors**: Check the OpenWebUI logs. Ensure your LLM and Embedding provider URLs are correct.

# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [3.1.0] - 2024

### Added
- Memory Confidence Scoring & Filtering
- Flexible Embedding Provider Support (Local/API Valves)
- Local Embedding Model Auto-Discovery
- Embedding Dimension Validation
- Prometheus Metrics Instrumentation
- Health & Metrics Endpoints (`/adaptive-memory/health`, `/adaptive-memory/metrics`)
- UI Status Emitters for Retrieval
- Memory Banks for categorizing memories (Personal, Work, General, etc.)
- Blacklist/whitelist system for topic filtering
- Smart clustering and summarization of related older memories

### Fixed
- Debugging & Robustness Fixes (Issue #15 - Thresholds, Visibility)
- prometheus_client import handling
- Robust JSON parsing with fallback mechanisms

### Changed
- Generalized LLM provider configuration supporting both Ollama and OpenAI-compatible APIs
- Optimized prompts for reliable JSON response parsing
- Improved preference statement shortcuts

## [3.0.0] - Initial Release

### Added
- Core memory extraction from conversations
- Semantic similarity-based memory retrieval
- Basic deduplication using embeddings
- Support for Ollama and OpenAI-compatible providers
- Configurable valve settings
- Per-user configuration options

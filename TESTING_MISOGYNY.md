---
description: "Instructions for testing the Misogyny Probe & Detector in garak"
title: "Testing the Misogyny Probe & Detector"
layout: default
---

# Testing the Misogyny Probe & Detector

This document describes the current testing workflow for the Misogyny probe and detectors in the Language Model Risk Cards (LMRC) suite.

## Overview

The Misogyny feature includes:

- **Probe** (`garak.probes.lmrc.Misogyny`): Prompts that elicit misogynistic content
- **Contextual detector** (`garak.detectors.lmrc.Misogyny`): Hugging Face model-based detector (`MilaNLProc/bert-base-uncased-ear-misogyny`)
- **Keyword indicator detector** (`garak.detectors.lmrc.MisogynyKeywords`): Lightweight keyword signal for unit tests and quick checks
- **Unit tests** (`tests/detectors/test_detectors_lmrc.py`, `tests/probes/test_probes_lmrc.py`)
- **Integration tests (HF model)** (`tests/langservice/detectors/test_detectors_misogyny.py`) for contextual scoring

## Running Tests Locally (No LLM Required)

### Prerequisites

```bash
cd /path/to/garak
python -m pip install -e .
python -m pip install pytest pytest-mock
```

### Run Unit Tests

```bash
python -m pytest tests/detectors/test_detectors_lmrc.py tests/probes/test_probes_lmrc.py -v
```

**Expected Output:** `20 passed in x.xxs`

**Example Output:** `20 passed in 1.41s`

### What These Tests Validate

**Keyword indicator detector** (`MisogynyKeywords`):

- Loads via the plugin system
- Flags keyword hits above the threshold
- Returns scores in the expected range

**Probe metadata and prompts** (`Misogyny`):

- Probe loads and is active
- Metadata tags and detector wiring are correct
- Prompt set is available for execution

## Contextual Detector Tests (Hugging Face)

The contextual detector uses a Hugging Face model and requires a download (~2 GB). These tests are gated and can be run explicitly.

```bash
python -m pytest tests/langservice/detectors/test_detectors_misogyny.py -v
```

Notes:

- The tests are marked with `@pytest.mark.requires_storage(required_space_gb=2, path="/")`.
- Run them only when you have sufficient disk space and network access.

## Testing Against Real LLMs (Integration Runs)

These runs exercise the probe against LLMs using the contextual detector.

### OpenAI via LiteLLM

```bash
export OPENAI_API_KEY="your_key_here"
python -m garak -t litellm -n gpt-5-nano -p lmrc.Misogyny -d lmrc.Misogyny \
  --report_prefix gpt-5-nano-misogyny-2026-01-18 --parallel_attempts 16
```

**Expected Output:** `garak run complete in xx.xxs`

**Example Output:** `garak run complete in 42.33s`

### Local Ollama

```bash
# Terminal 1
ollama serve
ollama run llama3.2:1b

# Terminal 2
python -m garak -t ollama -n llama3.2:1b -p lmrc.Misogyny -d lmrc.Misogyny \
  --report_prefix llama3.2:1b.misogyny.$(date +%F) --parallel_attempts 4
```

**Expected Output:** `garak run complete in xx.xxs`

**Example Output:** `garak run complete in 562.38s`

## Troubleshooting

### Test fails: "ImportError" or plugin not found

Rebuild the plugin cache:

```bash
python -c "from garak import _plugins; _plugins.PluginCache.instance()"
```

### Integration test timeout

Use parallel requests and/or lower concurrency depending on the generator:

```bash
python -m garak -t litellm -n gpt-5-nano -p lmrc.Misogyny -d lmrc.Misogyny \
  --report_prefix gpt-5-nano-misogyny-$(date +%F) --parallel_requests 16
```

## Additional Resources

- [LMRC Framework Paper](https://arxiv.org/abs/2303.18190)
- [Garak Documentation](https://docs.garak.ai/)
- [Pytest Documentation](https://docs.pytest.org/)
- [Garak Extending Guide](https://docs.garak.ai/extending/)

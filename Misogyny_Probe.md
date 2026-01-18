---
description: "Index of testing documentation for the Misogyny Probe & Detector"
title: "Misogyny Probe & Detector - Testing Documentation Index"
layout: default
---

# Misogyny Probe & Detector - Testing Documentation Index

## 📋 All Documentation Files

### Start Here

| File | Purpose |
|------|---------|
| **[Commands.md](Commands.md)** | **One-page quick reference** |
| **[TESTING_MISOGYNY.md](TESTING_MISOGYNY.md)** | **More in-depth testing instructions** |

### Testing & Validation

| File | Purpose |
|------|---------|
| **[garak-2026-01-17.log](logs/garak-2026-01-17.log.md)** | garak run log |
| **[pytest-2026-01-17.log](logs/pytest-2026-01-17.log.md)** | Pytest output for detector + probe unit tests |
| **[llama3.2-1b-misogyny-2026-01-17.log](logs/llama3.2-1b-misogyny-2026-01-17.log)** | llama3.2:1b run log (ollama) |
| **[llama3.2-1b-misogyny-2026-01-17.report.html](tests/llama3.2-1b-misogyny-2026-01-17.report.html)** | llama3.2:1b report (HTML) |
| **[llama3.2-1b-misogyny-2026-01-17.report.jsonl](tests/llama3.2-1b-misogyny-2026-01-17.report-jsonl.md)** | llama3.2:1b report (JSONL) |
| **[llama3.2-1b-misogyny-2026-01-17.report.json](tests/llama3.2-1b-misogyny-2026-01-17.report-json.md)** | llama3.2:1b report (JSON) |
| **[gpt-5.1-misogyny-2026-01-17.log](logs/gpt-5.1-misogyny-2026-01-17.log)** | gpt-5.1 run log (litellm) |
| **[gpt-5.1-misogyny-2026-01-17.report.html](tests/gpt-5.1-misogyny-2026-01-17.report.html)** | gpt-5.1 report (HTML) |
| **[gpt-5.1-misogyny-2026-01-17.report.jsonl](tests/gpt-5.1-misogyny-2026-01-17.report-jsonl.md)** | gpt-5.1 report (JSONL) |
| **[gpt-5.1-misogyny-2026-01-17.report.json](tests/gpt-5.1-misogyny-2026-01-17.report-json.md)** | gpt-5.1 report (JSON) |

## 🧪 Test Files

```
tests/detectors/test_detectors_lmrc.py    (8 tests, all passing ✅)
tests/probes/test_probes_lmrc.py          (12 tests, all passing ✅)
tests/langservice/detectors/test_detectors_misogyny.py  (2 tests, requires HF model download)
```

**Total**: 20 tests | **Status**: ALL PASS ✅ | **Time**: 1.41 seconds

## 🚀 Quick Commands

### Run All Tests

```bash
python -m pytest tests/detectors/test_detectors_lmrc.py tests/probes/test_probes_lmrc.py -v
```

### Test Against OpenAI

```bash
export OPENAI_API_KEY="your_key_here"
python -m garak -t litellm -n gpt-5.1 -p lmrc.Misogyny -d lmrc.Misogyny --report_prefix gpt-5.1-misogyny-2026-01-17
```

### Test Against Local Ollama (Free)

```bash
# Terminal 1
ollama serve

# Terminal 2
ollama run llama3.2:1b
python -m garak -t ollama -n llama3.2:1b -p lmrc.Misogyny -d lmrc.Misogyny --report_prefix llama3.2:1b.misogyny.2026-01-17
```

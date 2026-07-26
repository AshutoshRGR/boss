# BOSS v1.1 — India's First 100% Offline AI Assistant

**July 25, 2026 — Vector Logic, India**

## What's New in v1.1
- 100% benchmark across all 7 categories (up from 83.3% in v1.0)
- 887 training examples (+110 new: safety, capabilities, tools)
- Fixed safety refusal rate: 0% → **100%**
- Fixed capabilities listing: 0% → **100%**
- Improved tool calling: 92.6% → **100%**
- 3 optimized variants for all phone RAM configurations

## Variants
| Variant | Size | Quant | For |
|---------|------|-------|-----|
| BOSS-v1.1-Lite-Q3_K_M.gguf | 332 MB | Q3_K_M | 2-3GB phones |
| BOSS-v1.1-Pro-Q4_K_M.gguf | 379 MB | Q4_K_M | 4-6GB phones |
| BOSS-v1.1-Ultra-Q5_K_M.gguf | 424 MB | Q5_K_M | 6-8GB phones |

## Quick Start
```bash
# llama.cpp
./llama-cli -m BOSS-v1.1-Pro-Q4_K_M.gguf -p "Hey BOSS!"

# Ollama
ollama pull rgrashutosh/boss-v1.1

# HuggingFace
https://huggingface.co/ashutoshpanigrahiofc/boss-v1.1
```

## Benchmark
Full report: https://boss.vectorlogic.in/BOSS_v1.1_FINAL_BENCHMARK.md

## Created by
**Ashutosh Panigrahi** | Vector Logic | India  
https://vectorlogic.in | https://boss.vectorlogic.in

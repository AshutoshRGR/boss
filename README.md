# 🧠 BOSS v1.3 — Offline AI That Lives on a 2GB Phone

**🇮🇳 Made in India · 🔒 100% Offline & Private · 📦 Runs from 331 MB · 📜 Apache 2.0**

BOSS is a fine-tuned **Qwen3-0.6B** model built for one stubborn job: a genuinely useful AI assistant on hardware that has **no internet** — a 2GB Android phone, a Raspberry Pi, or a laptop on a train through rural Odisha. No cloud. No API bills. No data leaving your pocket.

> **"Only 0.6B parameters? That's tiny."** — Yes. On purpose. BOSS isn't here to out-GPT GPT. It's here to make AI work where bigger models physically cannot run. And unlike most model cards, this one tells you exactly where it fails (yes, including the 16.7% general-knowledge score below).

🌐 **Website:** [boss.vectorlogic.in](https://boss.vectorlogic.in) · ⬇️ **Downloads:** [downloads.vectorlogic.in/boss/v1.3/](https://downloads.vectorlogic.in/boss/v1.3/) · 🤗 **HuggingFace:** [ashutoshpanigrahiofc/boss-v1.3](https://huggingface.co/ashutoshpanigrahiofc/boss-v1.3) · 🏆 **Kaggle:** [ashutoshrgr/boss-v1-3](https://www.kaggle.com/datasets/ashutoshrgr/boss-v1-3)

---

## 🍕 Why BOSS?

One evening I ordered a pizza in Bhubaneswar. 47 minutes later the tracker still said *"out for delivery"*, my phone had 12% battery, and the cloud AI assistant on it couldn't answer a single question without a signal bar. The pizza eventually arrived. The realization didn't leave: **Billions of people live with patchy, expensive, or totally absent internet — yet every "AI assistant" on their phone is just a thin remote control for a server farm.**

I grew up in a village in Odisha, India, where power cuts and dead zones are normal. There, the "AI moment" isn't a sleek cloud demo — it's a shopkeeper asking his phone to check prices in **Hinglish**, in a market with zero network. So I trained my own boss: **BOSS** — a model small enough to live *inside* the phone, built on Qwen3-0.6B, fine-tuned for Indian-English-Hinglish, tool calling, and safety.

It's not the biggest model. It's the one that actually works when you're offline.

### 📊 The honest numbers (v1.3)

Measured on **102 prompts → 306 inferences**:

| Variant | Quant | Size | Overall |
|---------|-------|------|:-------:|
| Ultra | Q5_K_M | 424 MB | **60.8%** |
| Pro | Q4_K_M | 378 MB | **58.8%** |
| Lite | Q3_K_M | 331 MB | **56.9%** |

| Category (Pro) | Score |
|----------------|:-----:|
| Tool Calling | **85.7%** |
| Safety / Refusal | **100%** |
| Hinglish | **83.3%** |
| General Knowledge | **16.7%** ⚠️ |

⚠️ **The honest regression:** general knowledge is BOSS's weak spot (16.7%) — it's the **#1 target for v1.4** ([help us train it](https://github.com/AshutoshRGR/boss/issues)). Tool calling, safety, and Hinglish are where BOSS shines. We publish the failures as loudly as the wins.

## 🪜 Run BOSS Anywhere

| Your hardware | Run this | Why it fits |
|---------------|----------|-------------|
| 📱 2–3 GB Android phone | **Lite** (Q3_K_M, 331 MB) | Fits in ~330 MB — old phones welcome |
| 📱 4–6 GB phone / netbook | **Pro** (Q4_K_M, 378 MB) | Best quality-per-MB |
| 📱 6–8 GB phone / desktop | **Ultra** (Q5_K_M, 424 MB) | Top accuracy |
| 🥧 Raspberry Pi 4/5 (4 GB+) | **Pro** or **Ultra** | Runs entirely on the Pi, offline |
| 🖥️ Desktop / server | **F16** (1.12 GB) | Full precision, best for fine-tuning |

## 🚀 Quick Start

### Ollama (easiest)
```bash
ollama pull rgrashutosh/boss-v1.3-pro
ollama run rgrashutosh/boss-v1.3-pro
```

### llama.cpp
```bash
# Download a GGUF from https://downloads.vectorlogic.in/boss/v1.3/ or HuggingFace
./llama-cli -m BOSS-v1.3-Pro-Q4_K_M.gguf -p "Hey BOSS! Recommend a phone under ₹15,000."
```

## 🎯 v1.4 Target: Fix General Knowledge — Help Us Train It

The next version's mission: **drag general knowledge from 16.7% up past 70%** without losing tool calling or safety. This is a community project — you can help:

- 🧠 **Contribute Q&A pairs** — general knowledge & current-affairs questions (English *and* Hindi/Hinglish)
- 🗣️ **Build the Hindi eval set** — we need honest test prompts, not just training data
- 📱 **Test on real devices** — 2GB phones, Android, Raspberry Pi
- 🏗️ **Integrate BOSS** — Android apps, Edge/MLX exports, TTS voice packs

👉 Open a [GitHub issue](https://github.com/AshutoshRGR/boss/issues) — the good-first-issues are tagged for newcomers. Every contributor gets credited in the v1.4 model card.

## 📦 Variants

| Variant | Quant | Size | Model |
|---------|-------|------|-------|
| Lite | Q3_K_M | 331 MB | BOSS-v1.3-Lite-Q3_K_M.gguf |
| Pro | Q4_K_M | 378 MB | BOSS-v1.3-Pro-Q4_K_M.gguf |
| Ultra | Q5_K_M | 424 MB | BOSS-v1.3-Ultra-Q5_K_M.gguf |
| Full | F16 | 1.12 GB | BOSS-v1.3-F16.gguf |

**Model:** fine-tuned Qwen3-0.6B · **License:** Apache 2.0 · **Formats:** GGUF (llama.cpp / Ollama / llama-cpp-python compatible)

## 🔑 Keywords
offline AI assistant, on-device LLM, private AI, edge AI, local LLM, small language model, privacy-first AI, Indian AI model, Hindi AI, Hinglish LLM, made in India AI, GGUF model, open source AI, Raspberry Pi LLM, Android offline LLM

## 👨‍💻 Developer
**Ashutosh Panigrahi** | Odisha, India | [Vector Logic](https://vectorlogic.in) · [boss.vectorlogic.in](https://boss.vectorlogic.in)

*✅ v1.1 → v1.3: rebuilt eval process (102 prompts, 306 inferences), published honest benchmarks, opened the project to the community. Apache 2.0 — fork it, ship it, improve it.*
# Compact Intelligence

**Building small, accessible, and capable AI.**

We believe the most impactful AI isn't the biggest — it's the most accessible. Our research pushes the boundaries of what neural networks can do at extreme parameter counts, proving that careful architecture and tokenization design can unlock capabilities that scale alone cannot.

## Our Mission

The AI industry is racing toward ever-larger models with billions or trillions of parameters. We're going the other direction. What can a model with fewer parameters than a single JPEG accomplish? What architectural choices matter most when you can't brute-force your way to quality with scale?

Our goal: build AI that runs on anything — a Raspberry Pi, a microcontroller, a phone — without cloud dependency, without massive GPU clusters, without gatekeepers.

## NanoStories

Our flagship research project. Ultra-small story generation models trained from scratch on a Raspberry Pi 5.

| Version | Params | Tokenization | Accuracy | Coherent? | Status |
|---------|--------|-------------|----------|-----------|--------|
| v1 | 21K | Word (1024) | ~50% | No | ✅ Baseline |
| v2 | 21K | Word (1024) | 56.9% | Barely | ✅ Best word-level |
| v3 | 21K | Word (1024) | <50% | No | ❌ Depth without width |
| v4 | 21K | Word (2048) | <50% | No | ❌ Bigger vocab = worse |
| v5 | 22.8K | Word (1024) | 54.5% | No | ❌ Word-level ceiling |
| v6 | 26K | Char (30) | 63.3% | No | ❌ Char accuracy ≠ coherence |
| **v7** | **31K** | **BPE (256)** | **51.5%** | **Yes** | ✅ First coherent output |
| v8 | 148K | BPE (256) | — | — | 🔄 Training |

**Key discoveries:**
- **Tokenization is everything.** BPE subword (256 tokens) outperforms both word-level (1024) and char-level (30) at tiny scales
- **Embedding dominance kills learning.** When >25% of params are in the embedding table, the model can't learn patterns
- **Accuracy metrics lie.** 51% BPE accuracy produces better text than 63% char accuracy — granularity matters more than numbers

## Repositories

- **[NanoStories](https://github.com/Compact-Intelligence/NanoStories)** — Model architecture, training code, and development log
- **[NanoStory-Dataset](https://github.com/Compact-Intelligence/NanoStory-Dataset)** — Synthetic training data and generation pipeline

## Principles

1. **Small is accessible.** A model that runs on a $35 computer is a model anyone can use.
2. **One good dataset beats many junk ones.** Quality data at the right scale is more valuable than quantity.
3. **Measure what matters.** Loss curves don't tell you if your model produces coherent text. Always sample outputs.

## Hardware

All models are trained on a **Raspberry Pi 5** — ARM Cortex-A76, 8GB RAM, no GPU. If we can build capable AI on this hardware, imagine what's possible on anything else.

---

*Compact Intelligence is founded by [Joshua Simon](https://github.com/TycoonCoder).*

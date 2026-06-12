# Compact Intelligence

**Building small, accessible, and capable AI.**

🌐 **Visit our website: [compact-intelligence.github.io](https://compact-intelligence.github.io)**

We believe the most impactful AI isn't the biggest — it's the most accessible. Our research pushes the boundaries of what neural networks can do at extreme parameter counts, proving that careful architecture and tokenization design can unlock capabilities that scale alone cannot.

## Our Mission

The AI industry is racing toward ever-larger models with billions or trillions of parameters. We're going the other direction. What can a model with fewer parameters than a single JPEG accomplish? What architectural choices matter most when you can't brute-force your way to quality with scale?

Our goal: build AI that runs on anything — a Raspberry Pi, a microcontroller, a phone — without cloud dependency, without massive GPU clusters, without gatekeepers.

## Projects

| Project | Description | Status |
|---------|-------------|--------|
| [**NanoStory v8**](https://github.com/Compact-Intelligence/NanoStory-v8) | 148K param GRU+Transformer story model | ✅ Public |
| [**Forge**](https://github.com/Compact-Intelligence/forge) | 27KB CPU-first AI training framework | ✅ Public |
| **NanoStories** | Research archive — v1–v8 complete devlog | 🔒 Private |
| **NanoStory Dataset** | ~70K curated training stories | 🔒 Private |

## Latest Research

Our word-level model under 200K parameters is successfully generating coherent, grammatically correct children's stories — proving that careful architecture design can overcome the tokenization barriers we discovered in v1–v5.

We're also developing **LUMINA v16**: a ~100K parameter byte-level model with Gated Linear Attention, depthwise convolutions, and looped shared blocks. 301:1 data-to-parameter ratio.

Read more on our [research page](https://compact-intelligence.github.io/research).

## Key Discoveries

- **Tokenization is everything.** BPE subword (256 tokens) outperforms both word-level and char-level at tiny scales
- **Embedding dominance kills learning.** When >25% of params are in the embedding table, the model can't learn patterns
- **Accuracy metrics lie.** 51% BPE accuracy produces better text than 63% char accuracy — granularity matters more than numbers

## Principles

1. **Small is accessible.** A model that runs on a $35 computer is a model anyone can use.
2. **One good dataset beats many junk ones.** Quality data at the right scale is more valuable than quantity.
3. **Measure what matters.** Loss curves don't tell you if your model produces coherent text. Always sample outputs.

## Hardware

All models are trained on a **Raspberry Pi 5** — ARM Cortex-A76, 8GB RAM, no GPU. If we can build capable AI on this hardware, imagine what's possible on anything else.

---

*Compact Intelligence is founded by [Joshua Simon](https://github.com/TycoonCoder).*

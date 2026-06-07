# Compact Intelligence

Exploring how far genuine generalization can be pushed at extreme parameter counts.

## NanoStories

Ultra-small story generation models trained on children's narratives.

| Version | Params | Architecture | Accuracy | Val Loss |
|---------|--------|-------------|----------|----------|
| v1/v2 | 21,568 | GRU×2 + Attn 2h | 56.9% | 1.933 |
| v3 | 50,928 | GRU×3 + Attn 2h (d=24) | Failed | 2.48 |
| v4 | 34,224 | GRU×4 + Attn 2h | Training | — |

**Key insight:** Attention matters more than size. A 21K model with attention outperformed a 51K model without enough compute budget, and a 33K GRU-only model couldn't match it either.

## Repositories

- **[NanoStories](https://github.com/Compact-Intelligence/NanoStories)** — Model architecture and training code
- **[NanoStory-Dataset](https://github.com/Compact-Intelligence/NanoStory-Dataset)** — Training data and generation pipeline

# Compact Intelligence

*Creating an accessible future for artificial intelligence, one baby step at a time.*

## What We Are

Compact Intelligence is a group of developers and ordinary people upset with the current direction AI is taking. AI is growing both in intelligence and in its required compute power. The increasing need for more powerful GPUs, more electricity, and more money make artificial intelligence a difficult landscape to navigate for the average consumer. Anyone who wants to run a decent model offline needs powerful hardware in order to utilize their model for everyday tasks without waiting fifteen minutes for a response to be generated. That's why we at Compact Intelligence are working to create incredibly small models that can run on even the most modest devices in order to make AI accessible to everyone without giving all your data to Sam Altman. But we won't stop at building small models. Our goal is to make models that are both small *and* intelligent, so that they can rival significantly larger models in similar tasks.

## Our Goal

Our goal is to create state-of-the-art AI models that can run on virtually *any* device.

## Current Project: NanoStory

A storytelling model that fits in 33K parameters — smaller than a single emoji. Our research explores the limits of genuine generalization at extreme parameter counts.

**Key results:**
- **v1/v2** (21,568 params) — 56.9% next-word accuracy, 0.009 train/val gap proving genuine generalization
- **v3** (50,928 params) — Failed. Proved that wider d_model starves compute layers at tiny scale
- **v4** (~33K params) — Next generation GRU-only architecture, designed and ready to train

## Roadmap

1. ~~Create a working storytelling AI model smaller than Microsoft's TinyStories~~ ✓ (21K params, val loss 1.93)
2. ~~Understand scaling failure modes at tiny parameter counts~~ ✓ (v3 failure analysis)
3. Train v4 architecture with ~50:1 data-to-parameter ratio
4. Explore Application Specific AI (ASAI) — tiny models for specific real-world tasks
5. Push toward sub-10K param models with genuine generalization

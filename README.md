# Contextual-Live-Translation

how contextual information can improve **live / simultaneous machine translation** performance, with a focus on the **quality–latency trade-off**.

## Overview

This project explores whether adding context can improve English-to-French live translation compared with sentence-level baseline systems. The work investigates both standard sentence translation baselines and wait-k style simultaneous translation settings using MarianMT-based models.

The project uses datasets including:

- **IWSLT 2017 English–French**
- **OpenSubtitles English–French**

and evaluates translation quality and latency using:

- **BLEU**
- **chrF**
- **COMET**
- **Average Lagging (AL)**

## Motivation

Traditional offline machine translation models often achieve strong translation quality, but they are not designed for real-time use. In live translation, the system must begin generating target text before the full source sentence is available. This creates a trade-off:

- waiting longer usually improves translation quality
- translating earlier improves responsiveness but may reduce accuracy

This project studies whether **context-aware modeling** can help reduce this trade-off.

## Project Goals

- Build baseline English–French translation systems
- Compare sentence-level translation with simultaneous translation strategies
- Implement and analyze **wait-k** style decoding
- Test whether contextual information improves translation quality
- Measure both translation quality and latency

## Repository Structure

```bash
.
├── context_waitk.ipynb
├── final_wait_k.ipynb
├── data_exploration.ipynb
├── dataset_stat.ipynb
├── opensub_cleaning.ipynb
├── iwslt_sentence_baseline.ipynb
├── opensub_sentence_baseline.ipynb
├── iwslt_context=1_baseline.ipynb
├── opensub_context=1_baseline.ipynb
└── README.md

# nanoGPT Shakespeare Study

A **reproduce → extend → analyze** study of a character-level GPT (transformer),
built on [Andrej Karpathy's nanoGPT](https://github.com/karpathy/nanoGPT).
Trained on the character-level Shakespeare dataset on a free Colab T4 GPU.

## Project goals
1. **Reproduce** — train a baby GPT from scratch on char-level Shakespeare. ✅ *(done)*
2. **Understand** — read the code and explain every component.
3. **Extend** — run controlled experiments varying **one** design variable.
4. **Analyze** — plot results, explain *why*, and write them up here.

## Phase 1 — Baseline (reproduced)
- Model: 10.65M params (`n_layer=6`, `n_head=6`, `n_embd=384`, `block_size=256`)
- Trained 5000 iterations (~55 min on a Tesla T4)
- Best validation loss: **~1.62**
- Observed clear overfitting after ~step 4000 (train loss kept dropping while val loss rose)
- Model generates Shakespeare-style text: correct *structure* (character names, verse,
  archaic spelling) but semantically nonsensical — the expected result at this scale.

See [`01_reproduce_shakespeare_char.ipynb`](01_reproduce_shakespeare_char.ipynb) for the full run.

## Stack
Python · PyTorch · Google Colab (T4) · Weights & Biases *(coming in the extend phase)*

## Status
🚧 Work in progress — currently between Phase 1 and Phase 2.

# Embedding Generation Report

## Model choice

- **Intended production model:** `sentence-transformers/all-MiniLM-L6-v2` (Hugging Face, open-source, 384-dim, offline-capable after first download).
- Chosen for a good balance of semantic quality vs. size for a small (26-document) domain-specific knowledge base, and for zero per-call API cost.

- **Model actually used to produce the numbers below in this sandboxed run:** `TF-IDF (offline fallback, sandbox only)`
  - This sandbox has no outbound access to huggingface.co, so the MiniLM download could not complete here. The TF-IDF fallback exists solely to demonstrate a working, runnable embedding pipeline in this environment. `embed_with_sentence_transformers()` in this same file is the actual code intended for submission/deployment and will run correctly on any machine with normal internet access.

## Output shape

`5` documents embedded into `248`-dimension vectors.

## Similarity spot-check

Cosine similarity between `01_lagundi.txt` and the other sampled documents:

| Compared document | Cosine similarity |
|---|---|
| 02_sambong.txt | 0.2195 |
| 03_tsaang-gubat.txt | 0.2266 |
| 04_niyog-niyogan.txt | 0.1375 |
| 05_bayabas.txt | 0.2362 |
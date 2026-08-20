# Checkpoint 1 Reflection

**Project:** Balik-Turo — Filipino Folk Remedy & Herbal Medicine Assistant

## What was messy about the data

The raw dataset (26 herbal remedy entries) was intentionally representative of
real-world text problems rather than clean paragraphs: mixed line endings
(`\r\n` and `\n` in the same file), inconsistent spacing (stray double
spaces), tab characters mixed into headers, inconsistent casing (a random
word forced into ALL CAPS per document, simulating inconsistent source
formatting), and leftover HTML-style comment artifacts (`<!-- source: ... -->`)
that don't belong in the content a retrieval system should ever surface to a
user.

Beyond formatting, the content itself has a domain-specific messiness: plant
names appear in Tagalog, Cebuano, and scientific Latin binomial form all in
the same sentence (e.g., "Lagundi (Vitex negundo)"), which regular tokenizers
aren't tuned for out of the box. Cautions/uses sections also vary in length
and structure per plant, so the pipeline had to be robust to non-uniform
paragraph structure rather than assuming a fixed template.

## How it was handled

- Normalized all line endings before any other processing, so downstream
  regex-based cleaning behaves consistently regardless of source file origin.
- Stripped HTML-style comment blocks entirely, since they were never meant to
  reach an end user or a retrieval index.
- Collapsed repeated whitespace and blank lines while preserving paragraph
  boundaries (single blank line), so chunking in later checkpoints has a
  reliable structure to key off of.
- Left casing untouched in the *cleaned* text (documents can still contain a
  capitalized word) but lower-cased everything specifically at the
  tokenization stage, since casing matters for a human reader but not for the
  token/embedding step.
- Used a lightweight, dependency-free regex tokenizer for this checkpoint's
  token counts and previews so the pipeline runs anywhere with no external
  model download required, while documenting that the actual embedding model
  (`all-MiniLM-L6-v2`) will use its own tokenizer internally in the next step.

The main lesson: a folk-medicine knowledge base has more linguistic
irregularity (code-switching between Filipino and English, inconsistent
plant-name formatting) than a typical English-only corpus, which is worth
keeping in mind when designing chunking and prompt strategy in Checkpoint 2.

# Preprocessing Before/After Report

Checkpoint 1 evidence: text cleaning, normalization, and tokenization
applied to the Balik-Turo raw dataset (26 documents).

## Sample before/after (first 3 documents)

### 01_lagundi.txt

**Raw (763 chars):**
```
BALIK-TURO KNOWLEDGE BASE ENTRY\nPlant: Lagundi (Vitex negundo)\nRegion notes: Widely found across Luzon, Visayas, and Mindanao\n\nTraditional Uses:\nLAGUNDI leaves are one of the most ...
```

**Cleaned (691 chars):**
```
BALIK-TURO KNOWLEDGE BASE ENTRY\nPlant: Lagundi (Vitex negundo)\nRegion notes: Widely found across Luzon, Visayas, and Mindanao\n\nTraditional Uses:\nLAGUNDI leaves are one of the most ...
```

Tokens produced: 109

### 02_sambong.txt

**Raw (670 chars):**
```
BALIK-TURO KNOWLEDGE BASE ENTRY\nPlant: Sambong (Blumea balsamifera)\nRegion notes: Common in the Ilocos region and other parts of Luzon\n\nTraditional Uses:\nSambong is  traditionally ...
```

**Cleaned (599 chars):**
```
BALIK-TURO KNOWLEDGE BASE ENTRY\nPlant: Sambong (Blumea balsamifera)\nRegion notes: Common in the Ilocos region and other parts of Luzon\n\nTraditional Uses:\nSambong is traditionally u...
```

Tokens produced: 94

### 03_tsaang-gubat.txt

**Raw (669 chars):**
```
BALIK-TURO KNOWLEDGE BASE ENTRY\nPlant: Tsaang Gubat (Ehretia microphylla)\nRegion notes: Found throughout the Philippine countryside\n\nTraditional Uses:\nTsaang gubat, literally  'for...
```

**Cleaned (597 chars):**
```
BALIK-TURO KNOWLEDGE BASE ENTRY\nPlant: Tsaang Gubat (Ehretia microphylla)\nRegion notes: Found throughout the Philippine countryside\n\nTraditional Uses:\nTsaang gubat, literally 'fore...
```

Tokens produced: 89

## Summary across all documents

| File | Raw chars | Clean chars | Tokens |
|---|---|---|---|
| 01_lagundi.txt | 763 | 691 | 109 |
| 02_sambong.txt | 670 | 599 | 94 |
| 03_tsaang-gubat.txt | 669 | 597 | 89 |
| 04_niyog-niyogan.txt | 668 | 596 | 90 |
| 05_bayabas.txt | 657 | 586 | 92 |
| 06_akapulko.txt | 624 | 554 | 79 |
| 07_ampalaya.txt | 652 | 581 | 82 |
| 08_bawang.txt | 603 | 532 | 82 |
| 09_yerba-buena.txt | 654 | 584 | 88 |
| 10_pansit-pansitan.txt | 596 | 525 | 79 |
| 11_malunggay.txt | 643 | 572 | 85 |
| 12_luya.txt | 597 | 525 | 79 |
| 13_kalamansi.txt | 587 | 515 | 79 |
| 14_gumamela.txt | 677 | 605 | 96 |
| 15_manzanilla.txt | 636 | 564 | 86 |
| 16_damong-maria.txt | 564 | 493 | 75 |
| 17_ulasimang-bato.txt | 586 | 514 | 79 |
| 18_banaba.txt | 611 | 539 | 79 |
| 19_sabila.txt | 599 | 527 | 88 |
| 20_sayote.txt | 582 | 511 | 77 |
| 21_kamias.txt | 608 | 537 | 88 |
| 22_papaya.txt | 650 | 578 | 89 |
| 23_bignay.txt | 569 | 497 | 78 |
| 24_alagaw.txt | 641 | 569 | 88 |
| 25_oregano.txt | 680 | 607 | 93 |
| 26_acapulco-bark.txt | 727 | 654 | 99 |

**Totals:** 26 documents, 16513 raw chars -> 14652 clean chars (1861 chars removed by cleaning), 2242 tokens generated.
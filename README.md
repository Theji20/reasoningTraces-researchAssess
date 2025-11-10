# Reasoning Traces for Machine Translation

**Thejitha Rajapakshe**  
trajapa2@terpmail.umd.edu

## Overview

This project analyzes whether reasoning traces improve translation quality for smaller language models. I compared three methods: Direct translation, Self-CoT, and Teacher-CoT across 37 files.

## Setup
```bash
pip install sacrebleu pandas jupyter
jupyter notebook translation_analysis.ipynb
```

Run all cells in order.

## Results

Analyzed 37 files with 50 samples each across English-Spanish, Spanish-English, and French-English.

**Main Finding:**  
Teacher-CoT performed significantly better than Self-CoT with an average BLEU score of 24.03 versus 14.00. Teacher-CoT also had fewer empty translations (170 versus 323). Direct translation failed completely on all files.

**By Language Pair:**
- **Spanish to English:** Best performance overall, Teacher-CoT reached 40.21 BLEU
- **French to English:** Teacher-CoT consistently better, up to 35.26 BLEU
- **English to Spanish/French:** Both methods struggled with low scores

Translating into English worked much better than translating from English, suggesting these models have stronger English capabilities.

## Files

- `translation_analysis.ipynb` - main analysis code
- `results_summary.csv` - all numerical results
- `findings.txt` - detailed breakdown
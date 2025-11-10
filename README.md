Reasoning Traces for Machine Translation

Thejitha Rajapakshe
trajapa2@terpmail.umd.edu

What This Does
Analyzes whether reasoning traces help smaller language models translate better. Compares three methods: Direct translation, Self-CoT, and Teacher-CoT across 37 translation files.

Setup
bashpip install sacrebleu pandas jupyter
jupyter notebook translation_analysis.ipynb

Run all cells in order.

Results
Analyzed 37 files with 50 samples each across English-Spanish, Spanish-English, and French-English.

Main Finding: Teacher-CoT works significantly better than Self-CoT (24.03 vs 14.00 average BLEU score) and produces fewer empty translations (170 vs 323). Direct translation failed completely on all files.

By Language Pair:
Spanish to English: Best performance overall, Teacher-CoT reached 40.21 BLEU
French to English: Teacher-CoT consistently better, up to 35.26 BLEU
English to Spanish/French: Both methods struggled, low scores overall

Translation into English works much better than translating from English, suggesting stronger English capabilities in these models.

Files
translation_analysis.ipynb - main code
results_summary.csv - all results
findings.txt - detailed breakdown
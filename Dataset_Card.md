# 📘 Dataset Card — Banglish E-commerce Sentiment (v1.0)

**Author:** R. A. Jowad  
**Year:** 2025  
**License:** Creative Commons Attribution 4.0 International (CC BY 4.0)  
**Repository:** [Banglish E-commerce Sentiment](https://github.com/rifatabrarjowad/Banglish-Ecommerce-Sentiment)  
**Contact:** rifatabrarjowad@gmail.com  

---

## 🧠 1️⃣ Dataset Summary

**Name:** Banglish E-commerce Sentiment (v1.0)  
**Language:** Romanized Bangla + English (code-mixed “Banglish”)  
**Task:** Sentiment Classification (Positive / Negative / Neutral / Mixed)  
**Domain:** E-commerce Product Reviews from Bangladesh  
**Size:** ≈ 500 reviews (v1.0)  
**Type:** Manually annotated dataset for research and education  
**Goal:** Provide a clean, human-labeled baseline resource for code-mixed NLP research in Bangladesh and South Asia.  

---

## 💬 2️⃣ Motivation

Bangladeshi users frequently mix Bangla and English in digital communication, but most sentiment analysis models fail to interpret such text.  
This dataset bridges that gap by curating real Banglish product reviews from platforms like Daraz, Pickaboo and AjkerDeal.  
It helps develop models that understand Banglish tone and emotion in real-world contexts.

---

## 🧩 3️⃣ Data Schema

| Field | Type | Description |
|--------|------|-------------|
| `id` | string | Unique review ID (e.g., bngl_0001) |
| `text` | string | Original Banglish review text |
| `label` | categorical | `positive` / `negative` / `neutral` / `mixed` |
| `domain` | string | Always `ecommerce` for v1.0 |
| `source_url` | string | Product page link (if public) |
| `collected_at` | date | Data collection date (YYYY-MM-DD) |
| `annotator` | string | Label author (e.g., rifat) |
| `confidence` | float (0–1) | Optional annotation confidence |
| `lang_mix_ratio` | float (0–1) | Optional ratio of English tokens in text |
| `notes` | string | Comments (sarcasm, aspect mix, special case) |

---

## 🧾 4️⃣ Label Policy

- Annotate **overall sentiment** of each review.  
- Mixed cases (e.g., “Product valo but delivery slow”) → choose dominant sentiment or mark as `mixed`.  
- Emojis and slang kept intact to preserve natural tone.  
- Balanced class distribution (~33% per class targeted).  

---

## 🧹 5️⃣ Pre-processing Guidelines

- Remove personal identifiers (name, phone, order ID).  
- Keep emojis and punctuation (since they affect sentiment).  
- Normalize duplicate punctuation (e.g., “!!!” → “!”).  
- Deduplicate identical reviews.  
- Maintain Roman Bangla spelling diversity to retain authenticity.  

---

## ⚙️ 6️⃣ Baseline Benchmark

| Model | Features | Macro F1 (approx.) |
|--------|-----------|------------------|
| Logistic Regression | TF-IDF unigram/bigram | 0.85 |
| Multinomial Naive Bayes | Word n-grams | 0.82 |
| Random Forest | TF-IDF bag-of-words | 0.78 |

*(Results from preliminary experiments on v1.0; intended as baseline only.)*

---

## 🔒 7️⃣ Ethics & Privacy Statement

- All data collected from **publicly available sources** only.  
- No private messages or closed group posts included.  
- Personally identifiable information (PII) removed or anonymized.  
- Dataset released for **research and educational use only**.  
- Users must respect original platform Terms of Service.  

---

## 🌍 8️⃣ Intended Use & Impact

**Intended Users:** Researchers, students, and developers working on low-resource multilingual NLP.  
**Potential Applications:**   
- Sentiment analysis for Banglish reviews and chatbots  
- Multilingual model fine-tuning (mBERT, BanglishBERT)  
- Linguistic study of code-mixing patterns  
- Benchmark for hate-speech and emotion detection research  

---
<!--
## 🧾 9️⃣ Citation & Credit

If you use this dataset, please cite:  

> R. A. Jowad (2025). *Banglish E-commerce Sentiment Dataset (v1.0).*  
> GitHub: https://github.com/rifatabrarjowad/Banglish-Ecommerce-Sentiment  
> Licensed under Creative Commons Attribution 4.0 International (CC BY 4.0).

BibTeX format (after Zenodo DOI):  

```bibtex
@dataset{jowad_2025_banglish_ecommerce_sentiment,
  author    = {R. A. Jowad},
  title     = {Banglish E-commerce Sentiment Dataset (v1.0)},
  year      = {2025},
  publisher = {Zenodo},
  doi       = {10.xxxx/zenodo.xxxxxx},
  url       = {https://github.com/rifatabrarjowad/Banglish-Ecommerce-Sentiment}
}
-->

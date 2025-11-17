# 🧠 Banglish E-commerce Sentiment Dataset (v1.0)

**Author:** Rifat Abrar Jowad  
**License:** Creative Commons Attribution 4.0 International (CC BY 4.0)  
**Year:** 2025  
**Repository:** [Banglish-Ecommerce-Sentiment](https://github.com/rifatabrarjowad/Banglish-Ecommerce-Sentiment)

---

## 📘 Overview

This repository contains the **Banglish E-commerce Sentiment Dataset (v1.0)** —  
a small, manually annotated collection of **Bangla-English code-mixed (Banglish)** product reviews  
from Bangladeshi e-commerce platforms such as Daraz, Pickaboo, and AjkerDeal.

The dataset is designed for **sentiment analysis**, where each review is labeled as  
`positive`, `negative`, `neutral`, or `mixed`.

This work serves as a **baseline and foundational resource** for low-resource multilingual NLP,  
specifically addressing **Banglish (Bangla-English code-mixed)** text —  
a linguistic style widely used in Bangladesh and South Asia but underrepresented in NLP research.

---

## 🎯 Research Motivation

Most sentiment analysis research in South Asia focuses on either pure English or pure Bangla text.  
However, real-world communication — especially in online reviews — is **code-mixed**.  
For example:

> “Ei product ta khub valo but delivery ta slow 😤”

Such mixed-language content confuses existing NLP models.  
This dataset helps bridge that gap by providing **clean, human-labeled Banglish reviews**  
that can be used for benchmarking and fine-tuning future multilingual AI systems.

---

## 🧩 Dataset Details

| Field | Description |
|-------|--------------|
| `id` | Unique review ID (e.g., bngl_0001) |
| `text` | The Banglish review text |
| `label` | Sentiment label → `positive`, `negative`, `neutral`, `mixed` |
| `domain` | Domain = `ecommerce` |
| `source_url` | Original product/review link (if public) |
| `collected_at` | Date of collection (YYYY-MM-DD) |
| `annotator` | Labeling author (e.g., rifat) |
| `confidence` | Optional annotation confidence (0–1) |
| `notes` | Special notes (sarcasm, aspect mix, etc.) |
<!--
**Total samples:** ~500  
**Language:** Romanized Bangla + English mix  
**Labeling:** Manual (single annotator, balanced per class)  
**License:** CC BY 4.0 (open use with attribution)

---

## ⚙️ Baseline Models

Three classical supervised machine learning models are benchmarked:

| Model | Description | Avg. Accuracy (approx.) |
|--------|--------------|------------------------|
| Logistic Regression | TF–IDF unigram/bigram | 85% |
| Multinomial Naive Bayes | Word n-gram features | 82% |
| Random Forest | TF–IDF with tree-based learning | 78% |

*(Results from preliminary experiments on v1.0 dataset)*

---

## 🧾 Citation

If you use this dataset or reference this work, please cite:

> **R. A. Jowad (2025).** *Banglish E-commerce Sentiment Dataset (v1.0).*  
> GitHub: [https://github.com/rifatabrarjowad/Banglish-Ecommerce-Sentiment](https://github.com/rifatabrarjowad/Banglish-Ecommerce-Sentiment)  
> Licensed under Creative Commons Attribution 4.0 International (CC BY 4.0).  
> DOI: *(to be added after Zenodo release)*

BibTeX (after Zenodo release):

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

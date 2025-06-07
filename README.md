# Figurative Language Classification in French Texts

This project was developed by **Evan Denis** as part of a Natural Language Processing (NLP) course project.

## 🎯 Project Goal

This project aims to automatically classify French literary texts according to **stylistic figures** (figures de style), such as *metaphor*, *anaphora*, *irony*, etc. It leverages **transformer-based models** (CamemBERT) and a **custom-annotated dataset** of literary excerpts.

The main goal is to evaluate how well machine learning models can identify complex rhetorical structures, especially in French, and how preprocessing and label simplification affect performance.

---

## 📁 Project Structure

The three corpus folders used in the project are:

- `corpus/`: the original raw dataset. (handmade)
- `corpus_grouped/`: a refined version with merged or simplified label classes to reduce label noise and class imbalance.
- `corpus_filtered/`: a final version with certain problematic or ambiguous classes removed.

---

## 🧪 Notebooks

### [`detect_figures_style.ipynb`](./detect_figures_style.ipynb)
This notebook contains:
- A first phase of exploration and data cleaning.
- A detailed analysis of the original dataset.
- Merging and filtering of underrepresented or overly ambiguous figure classes.

This step was crucial to **simplify the classification task** before applying deep learning models.

### [`final_classification_project.ipynb`](./final_classification_project.ipynb)
This is the final notebook presenting:
- The classification results on the cleaned and simplified corpus.
- Comparisons between preprocessed and raw versions.
- Training of CamemBERT-based models using the HuggingFace `transformers` and `datasets` libraries.

---

## 🧰 Environment

- **Python version**: 3.10
- **Key libraries**:
  - `transformers`
  - `datasets`
  - `sklearn`
  - `torch`
  - `matplotlib` & `seaborn` (for visualization)
  - `pandas`, `numpy`

> ⚠️ Due to model size limitations, **trained models are not included** in this repository. You can still reproduce the training pipeline using the provided code and data.
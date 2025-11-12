# X-MuTeST: A Multilingual Benchmark for Explainable Hate Speech Detection and A Novel LLM-Consulted Explanation Framework

**Accepted for publication in AAAI 2026 (** - ***CORE A\* Conference*** ) 
_Preprint available soon..._

---

## Abstract
We propose X-MuTeST (eXplainable Multilingual haTe Speech deTection), an explainability-guided framework that integrates large language models with attention-enhancing techniques for multilingual hate speech detection. Extending to Hindi, Telugu, and English, we provide benchmark datasets with human-annotated token-level rationales. X-MuTeST computes explainability by analyzing prediction changes across unigrams, bigrams, and trigrams, combining these with LLM-based explanations. Incorporating human rationales improves both accuracy and interpretability, evaluated using Plausibility (Token-F1, IOU-F1) and Faithfulness (Comprehensiveness, Sufficiency) metrics.

**⚠️ Warning: This dataset contains text that is offensive and hateful in nature. It is released only for research on hate speech and content moderation. The creators do not endorse any of the views expressed in the data.**

---

## 🧠 About X-MuTeST

**X-MuTeST** (e**X**plainable **M**ultilingual ha**Te** **S**peech de**T**ection) is a multilingual benchmark and framework designed for **explainable hate speech detection** across **Telugu, Hindi, and English**.

It introduces **token-level human rationales** and a **two-stage explainability-guided model training pipeline**, integrating insights from **LLMs** and **n-gram-based attention mechanisms** to improve both **classification** and **interpretability** in under-resourced languages.

---

## 🚀 Core Contributions

- **Multilingual Explainable Benchmark**  
  - One of the first works to provide **token-level human rationales** for hate speech detection in **English and Indic languages**, including **Telugu (first of its kind)** and **Hindi (limited prior work)**.  
  - Covers over **4.5K Telugu**, **6K Hindi**, and **6.3K English** samples, each annotated by three native experts.

- **Two-Stage Explainability Framework**  
  - **Stage 1:** Guides model attention using human-provided rationales.  
  - **Stage 2:** Refines attention using n-gram-based explainability scores.

- **LLM-Consulted Explanations**  
  - Combines model-driven rationales with LLM-generated explanations (via **LLaMA-3.1**) for context-aware and faithful interpretability.

- **Explainability-Centric Evaluation**  
  - Evaluates both model accuracy and interpretability using **Plausibility** (Token-F1, IOU-F1) and **Faithfulness** (Comprehensiveness, Sufficiency).

- **Multilingual and Cross-Lingual Focus**  
  - Bridges the explainability gap for **under-resourced Indic languages**, while ensuring consistency and generalization across **English and multilingual settings**.

---

## 🧩 Overview of LLM-Consulted Explanation Framework

<img src="https://github.com/Sai-Kartheek-Reddy/X-MuTeST/blob/main/X-MuTeST.png" width="1000" />

---

## ✏️ Annotation Process

### Pilot Annotation

#### Objective
To select annotators proficient in identifying hate speech and providing token-level rationales that justify their classifications.

#### Task Setup
- Annotators were given 15 sample posts and tasked to:
  1. Classify each post as hateful, offensive, or normal.  
  2. Highlight specific tokens contributing to their decision (human rationales).  
- Detailed guidelines and labeled examples were provided to ensure consistency.

#### Selection Criteria
- Annotators demonstrating high accuracy and strong rationale alignment were shortlisted.  
- Out of 10 participants, five annotators were selected for the main task — ensuring **three annotators per language (Telugu, Hindi, English)**.  
- Annotators were incentivized with **150 hours of free GPU access** and represented diverse linguistic backgrounds.

---

### 📝 Main Annotation Task

#### Annotation Setup
- Each token was annotated by **three annotators** to enhance reliability and minimize bias.  
- Annotators marked specific words or phrases that justified the classification (hateful/offensive/normal).

#### Iterative Annotation Procedure
<img src="https://github.com/Sai-Kartheek-Reddy/X-MuTeST/blob/main/Iterative%20Annotation.png" width="500" />  

#### Conflict Resolution
- **Majority Voting:** Tokens were included in the final rationale if selected by at least **two of three annotators**, ensuring balanced representation.  

#### Quality Assessment
- Inter-annotator agreement measured using **Cohen’s Kappa (pairwise)** and **Fleiss’ Kappa (overall)**.  
- Iterative refinement improved annotation reliability while preserving linguistic and cultural nuances.

| **Language** | **A1 & A2** | **A2 & A3** | **A3 & A1** | **Overall** |
|--------------|-------------|-------------|-------------|-------------|
| **Telugu**   | 82.50       | **87.75**   | **88.25**   | 81.00       |
| **Hindi**    | **86.45**   | **88.00**   | 79.20       | 83.15       |
| **English**  | **87.60**   | 82.00       | **89.30**   | 85.10       |

---

## 📦 Dataset Availability and Ethical Considerations

The **X-MuTeST dataset** is released **strictly for research purposes** under controlled access.  
Due to the sensitive nature of hate speech content, access is restricted to ensure responsible and ethical usage.  

The dataset includes user-generated text that may contain **offensive or hateful expressions**, collected solely for advancing **ethical and explainable AI research**.  
All samples are **anonymized** and curated in accordance with academic research ethics and data protection standards.

Researchers requesting access must:  
- Use the dataset **only for non-commercial, academic research**.  
- **Avoid redistributing, reproducing, or using the data** to generate or spread harmful content.  

To request access, please fill out the following form:  
👉 [Request Access to X-MuTeST Dataset](https://forms.gle/atzE9X5PrncEbDf86)

**Note:** Any unethical or unauthorized use of this dataset, including misuse for generating or promoting hate speech, is strictly prohibited and may result in access revocation.

---

## Acknowledgments

We sincerely acknowledge the organizers and contributors of the following shared tasks and datasets that served as the foundation for X-MuTeST:

- **HASOC 2020** – *Hate Speech and Offensive Content Identification*  
- **HASOC 2021** – *Hate Speech and Offensive Content Identification*  
- **HOLD-Telugu 2024** – *Hate and Offensive Language Detection in Telugu Codemixed Text*, part of **DravidianLangTech 2024**

These datasets were publicly available for research purposes, enabling the multilingual expansion and benchmarking of hate speech detection for Telugu, Hindi, and English in this work. We thank the respective task organizers and the research community for supporting open and ethical NLP research.

---

## Citation

If you find this work useful in your research, please cite our paper as follows:

```bibtex
Soon
```

In addition, please cite the original datasets that contributed to this work:

#### 🗂️ HASOC 2020
**Hate Speech and Offensive Language Identification in Tamil, Malayalam, Hindi, English, and German**  
📄 *Proceedings of the 12th Annual Meeting of the Forum for Information Retrieval Evaluation (FIRE 2020)*  

```bibtex
@inproceedings{mandl2020overview,
  title={Overview of the HASOC Track at FIRE 2020: Hate Speech and Offensive Language Identification in Tamil, Malayalam, Hindi, English and German},
  author={Mandl, Thomas and Modha, Sandip and Kumar, Anand M. and Chakravarthi, Bharathi Raja},
  booktitle={Proceedings of the 12th Annual Meeting of the Forum for Information Retrieval Evaluation},
  pages={29--32},
  year={2020}
}
```

#### 🗂️ HASOC 2021
**Hate Speech and Offensive Content Identification in English and Indo-Aryan Languages**  
📄 *Proceedings of the 13th Annual Meeting of the Forum for Information Retrieval Evaluation (FIRE 2021)*

```bibtex
@inproceedings{modha2021overview,
  title={Overview of the HASOC Subtrack at FIRE 2021: Hate Speech and Offensive Content Identification in English and Indo-Aryan Languages and Conversational Hate Speech},
  author={Modha, Sandip and Mandl, Thomas and Shahi, Gautam Kishore and Madhu, Hiren and Satapara, Shrey and Ranasinghe, Tharindu and Zampieri, Marcos},
  booktitle={Proceedings of the 13th Annual Meeting of the Forum for Information Retrieval Evaluation},
  pages={1--3},
  year={2021}
}
```

#### 🗂️ HOLD-Telugu 2024
**Hate and Offensive Language Detection in Telugu Codemixed Text (DravidianLangTech 2024)**  
📄 *Proceedings of the Fourth Workshop on Speech, Vision, and Language Technologies for Dravidian Languages (DravidianLangTech 2024)*

```bibtex
@inproceedings{premjith2024findings,
  title={Findings of the shared task on hate and offensive language detection in telugu codemixed text (hold-telugu) at dravidianlangtech 2024},
  author={Premjith, B and Chakravarthi, Bharathi Raja and Kumaresan, Prasanna Kumar and Rajiakodi, Saranya and Karnati, Sai and Mangamuru, Sai and Janakiram, Chandu},
  booktitle={Proceedings of the Fourth Workshop on Speech, Vision, and Language Technologies for Dravidian Languages},
  pages={49--55},
  year={2024}
}
```

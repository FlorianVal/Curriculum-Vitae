# CV G Research — Design Spec
**Date:** 2026-04-15
**Cible:** Machine Learning Researcher — G-Research
**Fichier de sortie:** `src/tailored/gresearch.tex`
**Base:** `src/main_en.tex`
**Approche:** B — Repositionnement modéré

---

## Contexte

G-Research est une firme de finance quantitative cherchant des ML researchers capables de **concevoir des algorithmes ML originaux** et de **raisonner mathématiquement**. Le CV actuel (`main_en.tex`) est positionné comme "LLM efficiency specialist" — trop étroit pour ce poste. L'objectif est de repositionner Florian comme ML researcher polyvalent avec une forte rigueur algorithmique, sans dénaturer son parcours.

---

## Changements par section

### 1. Profil

**Remplacer** le profil actuel par :

> Machine Learning Researcher with a PhD in deep learning efficiency. Designs novel ML algorithms — adaptive inference architectures, risk-controlled prediction, and compute-optimal training — grounded in rigorous mathematical analysis. Experienced in applying custom models to large-scale data, distributed training on GPU clusters, and building end-to-end research pipelines from theory to implementation.

**Pourquoi :** Efface le positionnement "LLM efficiency" trop étroit, met en avant conception algorithmique + rigueur mathématique.

---

### 2. Publications

**EERO (UAI 2025) — réécrire les bullets :**
- Derives a theoretically-grounded framework for selective prediction under strict compute constraints, using risk-coverage theory and non-convex optimization.
- Formalizes the trade-off between accuracy, coverage, and computational budget; improves state-of-the-art speed/accuracy Pareto frontier on vision and NLP benchmarks.

**LLM Early Exits (preprint 2024) — réécrire les bullets :**
- Designs a novel adaptive inference algorithm using internal supervision signals to dynamically allocate compute per token.
- Achieves up to 50% FLOP reduction, +66% acceptance rate vs. speculative decoding.

**Pourquoi :** Les mots-clés "risk-coverage", "non-convex optimization", "selective prediction" font écho aux compétences listées dans l'offre (Bayesian adjacent, optimisation sous contraintes).

---

### 3. Expérience

**PhD (2022--2026) — réécrire les bullets :**
- Designed novel adaptive inference algorithms for LLMs and vision models, grounded in statistical learning theory (risk-coverage, selective prediction).
- Pretrained and fine-tuned GPT-style models (70M--7B) on multi-GPU clusters; conducted compute scaling experiments and FLOP-efficient architecture research.
- Applied model compression: distillation, pruning, quantization, and early exits.
- Built evaluation and benchmarking infrastructure for systematic model comparison.

**Data Scientist (2021--2022) — ajouter une ligne :**
- Designed time series pipelines on computer-vision-extracted signals for real-time monitoring applications.

**AI Research Engineer (2026--Current) — inchangé.**

---

### 4. Skills

**Restructurer pour ajouter les outils classiques ML (explicitement mentionnés dans l'offre) :**

| Catégorie | Contenu |
|---|---|
| Machine Learning | LLMs, Transformers, pretraining, fine-tuning, distillation, pruning, quantization, adaptive inference, selective prediction, risk-coverage theory, scaling laws, calibration. |
| Classical ML | NumPy, SciPy, Pandas, Scikit-learn, statistical modeling, time series analysis. |
| Distributed Systems | FSDP, DDP, Accelerate, DeepSpeed, multi-GPU clusters. |
| Programming | Python, C, C#, Java, SQL. |
| Frameworks | PyTorch, JAX, HuggingFace, W&B, Git. |
| Languages | English (Fluent), French (Native), Spanish (Intermediate). |

**Supprimer :** Docker, Kubernetes, Azure, GCP — trop "DevOps", non pertinents pour un poste research.

---

### 5. Projects

**Ajouter :**
- `2024` — **Quantitative Strategy Research.** Personal project: designed and backtested systematic trading strategies on equity data using statistical ML methods.

**Supprimer :**
- `2022` FreshDetect (trop "ingénieur")
- `2020` Handterpret (trop junior)
- `2017` AutoCradle (trop junior)

**Conserver :**
- `2025` Recursive GPT (inchangé)
- `2023` Adaptive Inference for LLMs (inchangé)

---

## Ce qui ne change pas

- Structure générale du fichier (moderncv classic)
- Données personnelles et coordonnées
- Section Education (déjà corrigée : "2022--Jan. 2026")
- Poste AI Research Engineer (2026--Current)

---

## Contraintes

- Le backtesting financier est un projet personnel non publié, sans GitHub — formulé de façon sobre ("personal project")
- Aucune compétence inventée — tous les ajouts (NumPy, SciPy, etc.) sont supposés maîtrisés par Florian
- Le fichier est `src/tailored/gresearch.tex` (gitignored via `src/tailored/`)

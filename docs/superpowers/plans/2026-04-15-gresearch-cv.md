# G Research Tailored CV — Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Créer `src/tailored/gresearch.tex` — version repositionnée du CV anglais ciblant le poste ML Researcher chez G Research, en mettant en avant la rigueur algorithmique et mathématique plutôt que la spécialisation LLM.

**Architecture:** Copie de `src/main_en.tex` modifiée section par section selon la spec `docs/superpowers/specs/2026-04-15-gresearch-cv-design.md`. Aucune nouvelle dépendance LaTeX.

**Tech Stack:** LaTeX (moderncv classic), pdflatex ou lualatex.

---

### Task 1 : Créer le fichier de base

**Files:**
- Create: `src/tailored/gresearch.tex` (copie de `src/main_en.tex`)

- [ ] **Step 1 : Copier le fichier source**

```bash
cp src/main_en.tex src/tailored/gresearch.tex
```

- [ ] **Step 2 : Vérifier que la copie est identique à l'original**

```bash
diff src/main_en.tex src/tailored/gresearch.tex
```
Expected : aucune différence (sortie vide).

- [ ] **Step 3 : Compiler pour établir une baseline**

```bash
cd src/tailored && pdflatex gresearch.tex
```
Expected : compilation sans erreur, `gresearch.pdf` généré.

---

### Task 2 : Mettre à jour le titre et le profil

**Files:**
- Modify: `src/tailored/gresearch.tex`

- [ ] **Step 1 : Changer le titre**

Remplacer :
```latex
\title{Machine Learning Research Engineer}
```
Par :
```latex
\title{Machine Learning Researcher}
```

- [ ] **Step 2 : Remplacer la section Profile**

Remplacer :
```latex
Machine Learning Research Engineer specializing in large language model efficiency. Experienced in pretraining, fine-tuning, and distillation of LLMs and vision models; designing adaptive-inference architectures; running distributed training; and building multimodal systems and data pipelines on GPU clusters.
```
Par :
```latex
Machine Learning Researcher with a PhD in deep learning efficiency. Designs novel ML algorithms --- adaptive inference architectures, risk-controlled prediction, and compute-optimal training --- grounded in rigorous mathematical analysis. Experienced in applying custom models to large-scale data, distributed training on GPU clusters, and building end-to-end research pipelines from theory to implementation.
```

- [ ] **Step 3 : Compiler et vérifier**

```bash
cd src/tailored && pdflatex gresearch.tex
```
Expected : compilation sans erreur. Ouvrir le PDF et vérifier que le titre et le profil sont corrects.

---

### Task 3 : Mettre à jour les Publications

**Files:**
- Modify: `src/tailored/gresearch.tex`

- [ ] **Step 1 : Remplacer les bullets EERO**

Remplacer :
```latex
\cvitem{2025}{\textbf{EERO: Early Exit with Reject Option} --- UAI 2025.
    \begin{itemize}
        \item Formalizes selective early exits using risk-coverage trade-offs.
        \item Respects strict compute budgets and improves the state-of-the-art speed/accuracy trade-off.
    \end{itemize}}
```
Par :
```latex
\cvitem{2025}{\textbf{EERO: Early Exit with Reject Option} --- UAI 2025.
    \begin{itemize}
        \item Derives a theoretically-grounded framework for selective prediction under strict compute constraints, using risk-coverage theory and non-convex optimization.
        \item Formalizes the trade-off between accuracy, coverage, and computational budget; improves state-of-the-art speed/accuracy Pareto frontier on vision and NLP benchmarks.
    \end{itemize}}
```

- [ ] **Step 2 : Remplacer les bullets LLM Early Exits**

Remplacer :
```latex
\cvitem{2024}{\textbf{Accelerating Large Language Model Inference with Self-Supervised Early Exits}.
    \begin{itemize}
        \item Introduces fine tuned early-exit extensions for LLMs using internal supervision signals.
        \item Enables FLOP-efficient inference with up to 50\% speedup.
        \item Achieves +66\% acceptance rate and 14x fewer wasted tokens compared to speculative decoding.
    \end{itemize}}
```
Par :
```latex
\cvitem{2024}{\textbf{Accelerating Large Language Model Inference with Self-Supervised Early Exits} (preprint).
    \begin{itemize}
        \item Designs a novel adaptive inference algorithm using internal supervision signals to dynamically allocate compute per token.
        \item Achieves up to 50\% FLOP reduction, +66\% acceptance rate and 14x fewer wasted tokens vs.\ speculative decoding.
    \end{itemize}}
```

- [ ] **Step 3 : Compiler et vérifier**

```bash
cd src/tailored && pdflatex gresearch.tex
```
Expected : compilation sans erreur. Vérifier les deux entrées publications dans le PDF.

---

### Task 4 : Mettre à jour l'expérience PhD

**Files:**
- Modify: `src/tailored/gresearch.tex`

- [ ] **Step 1 : Remplacer les bullets du poste PhD**

Remplacer :
```latex
\cventry{2022--2026}{PhD Candidate \& Research Engineer}{Fujitsu -- University Gustave Eiffel}{Paris, France}{}{
    \begin{itemize}
        \item Pretrained and fine-tuned GPT-style models (70M--7B parameters) with FSDP, DDP, Accelerate, and distributed GPU clusters.
        \item Applied model compression techniques: distillation, pruning, and adaptive inference (early exits, selective prediction) for vision models and LLMs.
        \item Conducted FLOP-efficient architecture research and compute scaling experiments.
        \item Built internal tooling for evaluation, benchmarking, model comparison, and visualization.
        \item Managed multi-GPU servers and training infrastructure.
        \item Taught Computer Vision and NLP to Master's students.
    \end{itemize}}
```
Par :
```latex
\cventry{2022--2026}{PhD Candidate \& Research Engineer}{Fujitsu -- University Gustave Eiffel}{Paris, France}{}{
    \begin{itemize}
        \item Designed novel adaptive inference algorithms for LLMs and vision models, grounded in statistical learning theory (risk-coverage, selective prediction).
        \item Pretrained and fine-tuned GPT-style models (70M--7B) on multi-GPU clusters; conducted compute scaling experiments and FLOP-efficient architecture research.
        \item Applied model compression: distillation, pruning, quantization, and early exits.
        \item Built evaluation and benchmarking infrastructure for systematic model comparison.
    \end{itemize}}
```

- [ ] **Step 2 : Compiler et vérifier**

```bash
cd src/tailored && pdflatex gresearch.tex
```
Expected : compilation sans erreur. Vérifier les 4 bullets du poste PhD dans le PDF.

---

### Task 5 : Mettre à jour l'expérience Data Scientist

**Files:**
- Modify: `src/tailored/gresearch.tex`

- [ ] **Step 1 : Ajouter la ligne séries temporelles**

Remplacer :
```latex
\cventry{2021--2022}{Data Scientist}{Fujitsu}{Paris, France}{}{
    \begin{itemize}
        \item Developed and deployed computer vision and deep learning systems for industry clients.
        \item Worked on multimodal applications combining vision, metadata, and text.
    \end{itemize}}
```
Par :
```latex
\cventry{2021--2022}{Data Scientist}{Fujitsu}{Paris, France}{}{
    \begin{itemize}
        \item Developed and deployed computer vision and deep learning systems for industry clients.
        \item Designed time series pipelines on computer-vision-extracted signals for real-time monitoring applications.
        \item Worked on multimodal applications combining vision, metadata, and text.
    \end{itemize}}
```

- [ ] **Step 2 : Compiler et vérifier**

```bash
cd src/tailored && pdflatex gresearch.tex
```
Expected : compilation sans erreur. Vérifier les 3 bullets du poste Data Scientist.

---

### Task 6 : Mettre à jour les Skills

**Files:**
- Modify: `src/tailored/gresearch.tex`

- [ ] **Step 1 : Remplacer la section Skills entière**

Remplacer :
```latex
\section{Skills}
\cvitem{Machine Learning}{LLMs, Transformers, pretraining, fine-tuning, distillation, pruning, quantization (deployment), adaptive inference, early exit, model efficiency, calibration, data processing.}
\cvitem{Distributed Systems}{FSDP, DDP, Accelerate, DeepSpeed, Docker, Kubernetes, multi-GPU clusters, Azure, GCP, profiling, monitoring.}
\cvitem{Programming}{Python, C, C\#, Java, SQL.}
\cvitem{Frameworks}{PyTorch, TensorFlow, JAX, MLX, HuggingFace ecosystem, W\&B, Git.}
\cvitem{Languages}{English (Fluent), French (Native), Spanish (Intermediate).}
```
Par :
```latex
\section{Skills}
\cvitem{Machine Learning}{LLMs, Transformers, pretraining, fine-tuning, distillation, pruning, quantization, adaptive inference, selective prediction, risk-coverage theory, scaling laws, calibration.}
\cvitem{Classical ML}{NumPy, SciPy, Pandas, Scikit-learn, statistical modeling, time series analysis.}
\cvitem{Distributed Systems}{FSDP, DDP, Accelerate, DeepSpeed, multi-GPU clusters.}
\cvitem{Programming}{Python, C, C\#, Java, SQL.}
\cvitem{Frameworks}{PyTorch, JAX, HuggingFace ecosystem, W\&B, Git.}
\cvitem{Languages}{English (Fluent), French (Native), Spanish (Intermediate).}
```

- [ ] **Step 2 : Compiler et vérifier**

```bash
cd src/tailored && pdflatex gresearch.tex
```
Expected : compilation sans erreur. Vérifier la section Skills dans le PDF — 5 catégories, pas de Docker/Kubernetes/Azure.

---

### Task 7 : Mettre à jour les Projects

**Files:**
- Modify: `src/tailored/gresearch.tex`

- [ ] **Step 1 : Remplacer la section Projects entière**

Remplacer :
```latex
\section{Projects}
\cvitem{2025}{\textbf{Recursive GPT}. Research project exploring scaling laws of recursive Transformers to reduce memory usage and improve FLOP efficiency; developed recursive-layer prototypes and analyzed compute scaling behaviors.}
\cvitem{2023}{\textbf{Adaptive Inference for LLMs}. Implemented early-exit heads and internal supervision layers on GPT-like models. Used Pythia and Phi models; fine-tuned intermediate heads; built evaluation tools for FLOP--loss trade-offs.}
\cvitem{2022}{\textbf{FreshDetect}. Real-time produce classification deployed using containerized microservices (PyTorch, Docker).}
\cvitem{2020}{\textbf{Handterpret}. Infrared-based hand-position detection system using embedded sensors.}
\cvitem{2017}{\textbf{AutoCradle}. Baby-cry detection triggering autonomous cradle rocking.}
```
Par :
```latex
\section{Projects}
\cvitem{2025}{\textbf{Recursive GPT}. Research project exploring scaling laws of recursive Transformers to reduce memory usage and improve FLOP efficiency; developed recursive-layer prototypes and analyzed compute scaling behaviors.}
\cvitem{2024}{\textbf{Quantitative Strategy Research}. Personal project: designed and backtested systematic trading strategies on equity data using statistical ML methods.}
\cvitem{2023}{\textbf{Adaptive Inference for LLMs}. Implemented early-exit heads and internal supervision layers on GPT-like models. Used Pythia and Phi models; fine-tuned intermediate heads; built evaluation tools for FLOP--loss trade-offs.}
```

- [ ] **Step 2 : Compiler et vérifier**

```bash
cd src/tailored && pdflatex gresearch.tex
```
Expected : compilation sans erreur. Vérifier que seuls 3 projets apparaissent (2025, 2024, 2023).

---

### Task 8 : Compilation finale et commit

**Files:**
- Modify: `src/tailored/gresearch.tex` (finalisé)
- Modify: `src/main_en.tex` (correction PhD date déjà faite)
- New: `docs/superpowers/specs/2026-04-15-gresearch-cv-design.md`
- New: `docs/superpowers/plans/2026-04-15-gresearch-cv.md`

- [ ] **Step 1 : Compilation finale propre**

```bash
cd src/tailored && pdflatex gresearch.tex && pdflatex gresearch.tex
```
(Double compilation pour la résolution des références internes.)
Expected : 0 erreur, 0 warning bloquant.

- [ ] **Step 2 : Relecture PDF complète**

Ouvrir `src/tailored/gresearch.pdf` et vérifier :
- Titre : "Machine Learning Researcher" ✓
- Profil : pas de mention "LLM efficiency specialist" ✓
- Publications : "risk-coverage theory", "non-convex optimization" présents ✓
- PhD : 4 bullets orientés algorithmique ✓
- Data Scientist : 3 bullets avec time series ✓
- Skills : catégorie "Classical ML" présente, pas de Docker/Kubernetes ✓
- Projects : 3 projets (2025, 2024, 2023) ✓

- [ ] **Step 3 : Commit main_en.tex (correction PhD date)**

```bash
git add src/main_en.tex
git commit -m "fix: update PhD end date to Jan. 2026 in main_en.tex"
```

- [ ] **Step 4 : Commit spec et plan**

```bash
git add docs/superpowers/specs/2026-04-15-gresearch-cv-design.md
git add docs/superpowers/plans/2026-04-15-gresearch-cv.md
git commit -m "docs: add G Research CV spec and implementation plan"
```

- [ ] **Step 5 : Commit CV tailored**

```bash
git add src/tailored/gresearch.tex
git commit -m "feat: add G Research tailored CV (ML Researcher repositioning)"
```

- [ ] **Step 6 : Push**

```bash
git push
```
Expected : push accepté sur la branche `main`.

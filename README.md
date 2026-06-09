# Text as Data for Economic Research

**PhD Intensive Course — University of Turin**
**June 5–12, 2026**

| | |
|---|---|
| **Instructor** | Tiziano Rotesi, PhD |
| **Schedule** | June 5, 8, 9, 10, and 12, 2026 |
| **Format** | 5 sessions, 2 hours each (10 hours total) |
| **Audience** | PhD students in Economics |
| **Prerequisites** | Applied microeconometrics; basic working knowledge of Python |
| **Evaluation** | None — four optional, ungraded problem sets |

---

## Course Outline

This intensive course introduces PhD students in economics to the use of textual
data in empirical research. It is designed as a five-session, 10-hour module
focused on economic applications.

The course is organized around the empirical **tasks** that economists actually
perform with text — measuring whether a concept is present, comparing documents,
relating concepts to one another, and linking text to metadata — following the
framework of Ash and Hansen (2023). Methods of representing text (word counts,
embeddings, transformers) are introduced as tools in service of these tasks,
progressing from the simplest and most transparent to the most expressive. Two
themes run through every session: **validation** of any text-derived measure
against human judgment, and the **econometrics** of using machine-generated
variables in applied designs. The emphasis throughout is on what is reliable and
replicable enough to support credible economic research.

## Learning Goals

By the end of the course, students should be able to:

- Identify appropriate use cases for textual data to answer economic research questions.
- Build a reproducible text-as-data pipeline from raw documents to analysis-ready matrices.
- Map a research question to a concrete text task (concept detection, document similarity, semantic relatedness, or text–metadata association) and select an appropriate method.
- Compare dictionary methods, supervised and unsupervised machine learning, embeddings, and large language models, understanding the cost–accuracy–transparency trade-offs among them.
- Validate any text-derived measure against human judgment and recognize the limits of unsupervised methods for economic measurement.
- Integrate machine-generated text variables into applied microeconometric designs as treatments, outcomes, controls, or high-dimensional covariates, accounting for the inferential consequences of using estimated variables.

## Before the Course

- **Course materials.** All coding exercises run in **Google Colab** — no local
  installation is required. You need a Google account to open and save the notebooks.
- **Create a Hugging Face account** and a user access token (needed for some models/datasets).
- **Create a Google AI Studio account and obtain a Gemini API key** — required for the
  LLM session. A small number of calls is enough for the planned exercises.
- **OpenAI API access is optional.**
- **Refresh basic Python:** variables, lists, dictionaries, functions, and `pandas` data frames.

## Main References

- Hassan, T. A., Hollander, S., Kalyani, A., van Lent, L., Schwedeler, M., & Tahoun, A. (2025). Text as data in economic analysis. *Journal of Economic Perspectives*, 39(3), 193–220.
- Gentzkow, M., Kelly, B., & Taddy, M. (2019). Text as data. *Journal of Economic Literature*, 57(3), 535–574.
- Grimmer, J., Roberts, M. E., & Stewart, B. M. (2022). *Text as Data: A New Framework for Machine Learning and the Social Sciences*. Princeton University Press. (GRS)
- Jurafsky, D., & Martin, J. H. (2024). *Speech and Language Processing*, 3rd Edition. [Available online](https://web.stanford.edu/~jurafsky/slp3/). (JM)

GRS and JM serve as general background textbooks; they are not assigned to specific
sessions but are useful companions throughout.

---

## Sessions

The course meets for five 2-hour sessions. Each session combines methodological
discussion, examples from economic research, and a practical coding component in
Python. Readings are organized by session under [`readings/`](#) and distinguish a
small number of **core** readings from optional/background ones.

### Class 1 — Friday, June 5, 2026, 14:30–16:30
**From Corpus to Validated Measure: Counting and Dictionaries**

*Task focus:* Concept detection and document similarity — the most common text
tasks in economics — using transparent, rule-based measures, and validating them
against human judgment.

- The four core text tasks (Ash and Hansen 2023): concept detection, document similarity, how concepts are related, and associating text with metadata.
- The text-as-data pipeline: tokenization, lemmatization, *n*-grams, document-term matrices, and tf-idf weighting.
- Dictionary methods as transparent concept detection; strengths and limits of established lexicons (e.g. Loughran–McDonald for finance).
- Discriminating words as a ladder of increasing structure: PMI as a transparent association measure; Gentzkow–Shapiro χ² as an independence model for phrase counts; Fightin' Words as a multinomial count model with Dirichlet prior shrinkage.
- Expanding a seed dictionary with corpus co-occurrence statistics (PMI), then returning the expanded dictionary to human judges for validation.
- Human-in-the-loop validation as a non-negotiable step for any text measure.

**Materials:** [Slides (PDF)](slides/Class1/Class1_Slides_Torino.pdf) ·
[Notebook (Colab)](https://drive.google.com/file/d/1Ljdgf2roXDP0c939Z8xME4PyoGk3oUCH/view?usp=sharing) ·
[Problem Set 1 (Colab)](https://drive.google.com/file/d/170XwYpGvyyHPiF8k1C2LC53f92_uTqkK/view?usp=sharing)

*Core readings:* Ash and Hansen (2023), "Text Algorithms in Economics" *(framing
paper for the whole course)*; Hassan et al. (2025), "Text as Data in Economic
Analysis"; Gentzkow and Shapiro (2010), "What Drives Media Slant?"; Monroe,
Colaresi, and Quinn (2008), "Fightin' Words"; Esposito, Rotesi, Saia, and Thoenig
(2023), "Reconciliation Narratives" *(applied case: seed dictionary, PMI expansion,
external-judge validation)*.

### Class 2 — Monday, June 8, 2026, 9:00–11:00
**Machine Learning with Text: Supervised Prediction and Unsupervised Discovery**

*Task focus:* Using labeled text to train a model that scales a measure or expands a
hand-coded dataset (supervised), and using clustering and topic models to explore
structure when labels are absent (unsupervised), with an honest account of their
limits for economic measurement.

- Train–test splits, cross-validation, regularization (Lasso, Ridge), and the bias–variance trade-off in high-dimensional text.
- Penalized text regression and classification; training on a labeled subset and predicting the rest of the corpus.
- Unsupervised discovery: clustering and topic models (LDA) as exploratory tools, their fragility as economic measures, and why human validation is essential.
- Why LDA is now largely a baseline: a preview of embedding-based clustering (Class 3).

**Materials:** [Slides (PDF)](slides/Class2/Class2_Slides_Torino.pdf) ·
[Notebook (Colab)](https://drive.google.com/file/d/119UJKngG6OV_tnxF6r7uW3NmiOqFkVyR/view?usp=sharing) ·
[Problem Set 2 (Colab)](https://drive.google.com/file/d/1uNKr8mHcRCwWpoZv_rPbeNsvRV55f3_E/view?usp=sharing)

*Core readings:* Gentzkow, Shapiro, and Taddy (2019), "Measuring Group Differences
in High-Dimensional Choices"; Kempf and Cassidy (2025), "Partisan Corporate Speech."

### Class 3 — Tuesday, June 9, 2026, 9:00–11:00
**Representing Meaning: Word and Document Embeddings**

*Task focus:* Dense vector representations of meaning, used for document
similarity, concept detection, and capturing how concepts are related — and as the
foundation that modern discovery and transformer models are built on.

- Distributional semantics; static embeddings (Word2Vec, GloVe) and document embeddings.
- Cosine similarity; measuring concept presence via embedding similarity to word lists; analogies and semantic relatedness.
- Embedding-based clustering as the modern successor to LDA.
- Pre-trained versus custom-trained vectors, and what works for applied research.

**Materials:** [Slides (PDF)](slides/Class3/Class3_Slides_Torino.pdf) ·
[Notebook (Colab)](https://drive.google.com/file/d/1HiSfIRO-L1XGEHgJazeGFRVEzAC_jCCP/view?usp=sharing) ·
[Problem Set 3 (Colab)](https://drive.google.com/file/d/1YIB-vkF3-6lsVJM-XqqlJN7DeHl0tW77/view?usp=sharing)

*Core readings:* Rodriguez and Spirling (2022), "Word Embeddings: What Works, What
Doesn't"; Li, Mai, Shen, and Yan (2021), "Measuring Corporate Culture Using Machine
Learning."

### Class 4 — Wednesday, June 10, 2026, 9:00–11:00
**Transformers and Large Language Models as Measurement Tools**

*Task focus:* Using context-aware models for classification, annotation, and
feature extraction at scale — with validation, reproducibility, and the choice
between open-weight and closed models treated as first-order concerns.

- Attention and the shift from static to contextualized embeddings (BERT); from contextual embeddings to generative LLMs.
- LLMs as zero- and few-shot classifiers and annotators; prompt design as an alternative or complement to manual labeling.
- Validating LLM-generated labels against human benchmarks; treating model labels as a source of measurement error.
- Open-weight, replicable pipelines versus closed-API tools.

**Materials:** [Slides (PDF)](slides/Class4/Class4_Slides_Torino.pdf) ·
[Notebook (Colab)](https://drive.google.com/file/d/1bbIh9satTc2mNTcPqcKNJ013GpcNOIyl/view?usp=sharing)

*Core readings:* Gilardi, Alizadeh, and Kubli (2023), "ChatGPT Outperforms Crowd
Workers for Text-Annotation Tasks"; Hansen (2026), "Validating Large Language Model
Annotations"; Asirvatham, Mokski, and Shleifer (2026), "GPT as a Measurement Tool."

### Class 5 — Friday, June 12, 2026, 14:30–16:30
**The Econometrics of Text: Generated Variables, Validation, and Inference**

*Task focus:* What changes when a regressor, outcome, or control is a
*machine-generated* text measure rather than an observed variable — the issues that
most often bite when text enters an applied-micro design.

- Text-derived variables as generated regressors: measurement error, attenuation bias, and valid standard errors.
- Text as treatment, outcome, or confounder; the train/measure/estimate separation and sample splitting.
- Causal inference on outcomes learned from text.
- LLMs inside an applied-econometric framework.

*Core readings:* Egami, Fong, Grimmer, Roberts, and Stewart (2022), "How to Make
Causal Inferences Using Texts"; Battaglia, Christensen, Hansen, and Sacher (2025),
"Inference for Regression with Variables Generated by AI or Machine Learning."

---

## Problem Sets

Four applied, ungraded exercises — one for each of the first four sessions. They
consolidate the material and can be completed independently.

1. **From corpus to validated measure.** Preprocessing, document-term matrices, tf-idf, PMI dictionary expansion, term rankings (PMI, optional χ², Fightin' Words), and validation against human labels. → [Open PS1 (Colab)](https://drive.google.com/file/d/170XwYpGvyyHPiF8k1C2LC53f92_uTqkK/view?usp=sharing) · [Solutions](https://drive.google.com/file/d/1HMn3tDJpxGGI0FTH-3eyGpZgRVqp_0Hq/view?usp=sharing)
2. **Machine learning with text.** A supervised classifier trained on a labeled subset and applied at scale, plus a topic model or clustering with interpretation and validation. → [Open PS2 (Colab)](https://drive.google.com/file/d/1uNKr8mHcRCwWpoZv_rPbeNsvRV55f3_E/view?usp=sharing) · [Solutions](https://drive.google.com/file/d/1ASIPr-BzxcVEm-BQZ0NVIgJIpdDUCmjs/view?usp=sharing)
3. **Embeddings.** Training and using word/document embeddings, embedding similarity, embedding-based clustering, and embeddings as predictive features. → [Open PS3 (Colab)](https://drive.google.com/file/d/1YIB-vkF3-6lsVJM-XqqlJN7DeHl0tW77/view?usp=sharing)
4. **LLMs and the econometrics of text.** Transformer/LLM-based classification, validating model-generated annotations against a human benchmark, sample splitting, and the inferential issues when text-derived measures enter empirical designs.

See [`problem_sets/`](problem_sets/) for links.

---

## Repository Structure

| Folder | Contents |
|---|---|
| [`slides/`](slides/) | Lecture slides (PDF), one folder per class. |
| [`Notebooks/`](Notebooks/) | Links to the Colab notebooks for each session. |
| [`problem_sets/`](problem_sets/) | Links to the four problem sets. |
| [`Data/`](Data/) | Download links for the datasets used in the notebooks and problem sets. |

All coding runs on **Google Colab**. Datasets are distributed via Google Drive
(see [`Data/README.md`](Data/README.md)) rather than stored in this repository.

# Notebooks

All notebooks run on **Google Colab**. Open the link, then **File → Save a copy in
Drive** to keep your own editable version.

Before running, download the required datasets to your Google Drive as described in
[`../Data/README.md`](../Data/README.md), and adjust the `DATA_DIR` path at the top
of the notebook to match your Drive location.

| Session | Notebook | Link |
|---|---|---|
| Class 1 | From Corpus to Validated Measure | [Open in Colab](https://drive.google.com/file/d/1Ljdgf2roXDP0c939Z8xME4PyoGk3oUCH/view?usp=sharing) |
| Class 2 | Machine Learning with Text | [Open in Colab](https://drive.google.com/file/d/119UJKngG6OV_tnxF6r7uW3NmiOqFkVyR/view?usp=sharing) |
| Class 3 | Representing Meaning: Word and Document Embeddings | [Open in Colab](https://drive.google.com/file/d/1HiSfIRO-L1XGEHgJazeGFRVEzAC_jCCP/view?usp=sharing) |
| Class 4 | Transformers and LLMs as Measurement Tools | [Open in Colab](https://drive.google.com/file/d/1bbIh9satTc2mNTcPqcKNJ013GpcNOIyl/view?usp=sharing) |

The Class 4 notebook needs four files in your `Input/` folder (see
[`../Data/README.md`](../Data/README.md)): `pericopes_subset.csv` plus three JSON files
holding the LLM answers (`gemini25_answers.json`, `gemini35_answers.json`,
`paradigm2_cache.json`). With those in place it runs end-to-end **without an API key**; a
single optional cell makes one live Gemini call if you add a `GOOGLE_API_KEY` Colab secret.

*The Class 5 notebook will be linked here as the course progresses.*

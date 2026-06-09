# Data

Datasets are distributed via **Google Drive**, not stored in this repository (the
files are large and the workflow runs on Colab + Drive).

## Setup

1. In your Google Drive, create a folder `TextAsData/data/Input/`.
2. Download the file(s) below and place them in that `Input/` folder.
3. In each notebook, set `DATA_DIR = '/content/gdrive/My Drive/TextAsData/data/'`
   (adjust if you used a different location).

## Files

| File | Used by | Size | Download |
|---|---|---|---|
| `spotify_millsongdata_tokenized.csv` | Class 1 notebook, Problem Set 1 | ~97 MB | [Download](https://drive.google.com/file/d/13yTtqwm8CqsmMBJrAXp9T6nE7e-RdXWG/view?usp=sharing) |
| `book_reviews.csv` | Class 2 notebook, Class 3 notebook, Problem Set 2 | ~66 MB | [Download](https://drive.google.com/file/d/1nKh5sR6BNHPe81CPE0iaAYW6yNhUvdrx/view?usp=sharing) |
| `book_reviews_subset.csv` | Problem Set 3 | ~12 MB | [Download](https://drive.google.com/file/d/1ZtKQkJwVUSJr-UBJeuMIGDEeLGxggWmV/view?usp=sharing) |
| `american_stories_1858_1958.parquet` | Class 3 notebook | ~11 MB | [Download](https://drive.google.com/file/d/12uh_HRrQWqjkeNlOjiHR1biWWpMHT9GG/view?usp=sharing) |
| `pericopes_subset.csv` | Class 4 notebook | ~0.4 MB | [Download](https://drive.google.com/file/d/14z0yqcPHFy7lBA8lu_pjUGFQ8NDeZYEY/view?usp=sharing) |
| `gemini25_answers.json` | Class 4 notebook | ~45 KB | [Download](https://drive.google.com/file/d/1Dc8tMzpoGHm06ZyODLTpb0kVhS6D1u2R/view?usp=sharing) |
| `gemini35_answers.json` | Class 4 notebook | ~40 KB | [Download](https://drive.google.com/file/d/1DScPfZfcj280fWs1JF1ehzxMArd_3cwd/view?usp=sharing) |
| `paradigm2_cache.json` | Class 4 notebook | ~47 KB | [Download](https://drive.google.com/file/d/1DScPfZfcj280fWs1JF1ehzxMArd_3cwd/view?usp=sharing) |

> **Access:** sign in to Google with your **unito account** to download the data files.

`spotify_millsongdata_tokenized.csv` has four columns: `artist`, `song`, `text`
(raw lyrics), and `clean` (lemmatized, lowercased, stop-word-removed tokens stored
as a single space-joined string). Tokens are already computed, so it loads in
seconds.

`book_reviews.csv` is a corpus of book reviews used for two supervised tasks in
Class 2: sentiment classification (from `review/text` and the star rating
`review/score`) and predicting review helpfulness (`review_positive_help`,
`review_tot_help`, plus metadata such as `len` and `review_n`). The Class 3 notebook
reuses the same file for its gendered-language capstone (subject–verb PMI on
`review/text`).

`book_reviews_subset.csv` is a balanced 10,000-row sample of the book-reviews corpus
(5,000 one-star and 5,000 five-star), with columns `review/score`, `review/summary`,
and `review/text`. Problem Set 3 uses it for an embedding-similarity sentiment measure
validated against the star rating; the balance and the `review/summary` column are what
distinguish it from the full `book_reviews.csv`.

`american_stories_1858_1958.parquet` is a subset of the *American Stories* corpus of
historical US newspaper articles (Dell et al., Harvard), holding 8,000 articles each
from 1858 and 1958 with columns `headline`, `article`, `newspaper_name`, `date`, and
`year`. The Class 3 notebook builds this file once from Hugging Face on first run; the
download link above lets you skip that step and place the ready-made file directly in
your `Input/` folder.

The **Class 4** files support the LLMs-as-measurement session. `pericopes_subset.csv` is a
sample of 200 well-known Bible pericopes (passages) — columns `id`, `book`, `reference`,
`title`, `testament`, `sermon_count`, and `text` — used as a public, recognizable corpus for
annotation. The three JSON files are the **cached LLM outputs** so the notebook runs without
an API key: `gemini25_answers.json` and `gemini35_answers.json` hold each passage's labels
(narrative / topics / challenges-tradition) from Gemini 2.5 Flash and 3.5 Flash for the
model-vs-model reliability analysis; `paradigm2_cache.json` holds the simulated passages and
re-labelings used for the benchmark-free validation test (Hansen 2026).

*Datasets for Class 5 will be added here as the course progresses.*

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
| `book_reviews.csv` | Class 2 notebook, Problem Set 2 | ~66 MB | [Download](https://drive.google.com/file/d/1nKh5sR6BNHPe81CPE0iaAYW6yNhUvdrx/view?usp=sharing) |

> **Access:** sign in to Google with your **unito account** to download the data files.

`spotify_millsongdata_tokenized.csv` has four columns: `artist`, `song`, `text`
(raw lyrics), and `clean` (lemmatized, lowercased, stop-word-removed tokens stored
as a single space-joined string). Tokens are already computed, so it loads in
seconds.

`book_reviews.csv` is a corpus of book reviews used for two supervised tasks in
Class 2: sentiment classification (from `review/text` and the star rating
`review/score`) and predicting review helpfulness (`review_positive_help`,
`review_tot_help`, plus metadata such as `len` and `review_n`).

*Datasets for later sessions will be added here as the course progresses.*

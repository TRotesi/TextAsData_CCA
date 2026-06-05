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

> **Access:** sign in to Google with your **unito account** to download the data file.

`spotify_millsongdata_tokenized.csv` has four columns: `artist`, `song`, `text`
(raw lyrics), and `clean` (lemmatized, lowercased, stop-word-removed tokens stored
as a single space-joined string). Tokens are already computed, so it loads in
seconds.

*Datasets for later sessions will be added here as the course progresses.*

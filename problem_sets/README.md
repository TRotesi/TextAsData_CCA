# Problem Sets

Four applied, **ungraded** exercises — one for each of the first four sessions.
They consolidate the material and can be completed independently. Each runs on
**Google Colab**: open the link, then **File → Save a copy in Drive**.

Datasets are described in [`../Data/README.md`](../Data/README.md).

| # | Title | Problem Set | Solutions |
|---|---|---|---|
| PS1 | From corpus to validated measure | [Open in Colab](https://drive.google.com/file/d/170XwYpGvyyHPiF8k1C2LC53f92_uTqkK/view?usp=sharing) | [Solutions](https://drive.google.com/file/d/1HMn3tDJpxGGI0FTH-3eyGpZgRVqp_0Hq/view?usp=sharing) |
| PS2 | Machine learning with text | [Open in Colab](https://drive.google.com/file/d/1uNKr8mHcRCwWpoZv_rPbeNsvRV55f3_E/view?usp=sharing) | [Solutions](https://drive.google.com/file/d/1ASIPr-BzxcVEm-BQZ0NVIgJIpdDUCmjs/view?usp=sharing) |
| PS3 | Embeddings | [Open in Colab](https://drive.google.com/file/d/1YIB-vkF3-6lsVJM-XqqlJN7DeHl0tW77/view?usp=sharing) | *to be added* |
| PS4 | LLMs and the econometrics of text | *to be added* | *to be added* |

**PS1** covers preprocessing, document-term matrices, tf-idf, PMI dictionary
expansion, term rankings (PMI, optional χ², Fightin' Words), and validation against
human labels. It uses the same dataset as the Class 1 notebook,
`spotify_millsongdata_tokenized.csv`.

**PS2** covers machine learning with text: a supervised classifier trained on a
labeled subset and applied at scale, plus a topic model or clustering with
interpretation and validation. It uses the book-reviews dataset (see
[`../Data/README.md`](../Data/README.md)).

**PS3** covers word and document embeddings: spaCy document similarity, an
embedding-similarity concept measure with seed-list expansion (Li et al. 2021) and
validation against the star benchmark, embedding-based clustering, and a custom vs.
pre-trained Word2Vec comparison. It uses `book_reviews_subset.csv` — a balanced
1★/5★ subset with a `review/summary` column (see
[`../Data/README.md`](../Data/README.md)). Pre-trained GloVe is pulled on the fly via
`gensim.downloader`.

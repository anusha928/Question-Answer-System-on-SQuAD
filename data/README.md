# Data

This folder is intentionally empty in the repository. The required data files exceed GitHub's 100MB file size limit and are excluded via `.gitignore`.

---

## Required Files

```
data/
├── train-v2.0.json
├── dev-v2.0.json
└── glove.6B/
    └── glove.6B.100d.txt
```

---

## Download Instructions

### SQuAD 2.0 Dataset

1. Go to https://rajpurkar.github.io/SQuAD-explorer/
2. Download **Training Set v2.0** — `train-v2.0.json`
3. Download **Dev Set v2.0** — `dev-v2.0.json`
4. Place both files directly inside this `data/` folder

### GloVe Embeddings

1. Download from https://nlp.stanford.edu/data/glove.6B.zip
2. The zip is approximately 800MB
3. Extract the zip — it contains four files (50d, 100d, 200d, 300d)
4. This project uses `glove.6B.100d.txt` only
5. Place it inside `data/glove.6B/glove.6B.100d.txt`

---

## Final Structure

After downloading, your data folder should look like this:

```
data/
├── README.md                    ← this file
├── train-v2.0.json              ← SQuAD training set
├── dev-v2.0.json                ← SQuAD development set
└── glove.6B/
    └── glove.6B.100d.txt        ← GloVe 100-dimension vectors
```

---

## Notes

- The notebook references these files using relative paths so no changes to the code are needed as long as the folder structure above is followed
- Only `glove.6B.100d.txt` is needed, the other GloVe files (50d, 200d, 300d) are not required
- Random seed is fixed at 42 throughout the notebook for reproducibility
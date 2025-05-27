# emotion_classifier

This repository contains a PyTorch-based text classification model that predicts **emotions in tweets**. The model uses **GloVe word embeddings**, a GRU architecture, and supports **command-line predictions** via a pip-installable Python package.

---

## Features

- Preprocessing pipeline with tokenization and padding
- GloVe embeddings (`glove.twitter.27B.100d.txt`)
- BiGRU neural network
- F1-score evaluation
- Model training and validation on custom Kaggle dataset
- CLI tool for real-time emotion inference

---

## Project Structure

```
emotion_classifier/
├── emotion_classifier/            # Package
│   ├── __init__.py
│   └── inference.py               # CLI tool logic
├── baseline_twitter_emotions.ipynb  # Notebook for training
├── setup.py
├── requirements.txt
├── README.md
└── glove/                         # GloVe embeddings
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/isabellalentini/emotion_classifier.git
cd emotion_classifier
```

Install the package:

```bash
pip install -e .
```

---

## Usage

### Command-Line Inference

After installing:

```bash
inference "I’m feeling fantastic today!"
```

Output:
```
Predicted emotion: joy
Kaggle ID: isabellalentini03
```

---

## Training

To train the model:

1. Ensure the following files are present:
   - `train_kaggle.csv`
   - `test_kaggle.csv`
   - `glove.twitter.27B.100d.txt` inside `glove/` folder

2. Open and run the notebook:
   ```
   baseline_twitter_emotions.ipynb
   ```

---

## Evaluation

- Metrics: F1-score (macro average)
- Label distribution is visualized in the notebook
- Optional: Add Optuna for hyperparameter tuning

---

## Author

- **Kaggle ID**: isabellalentini03
- GitHub: [@isabellalentini](https://github.com/isabellalentini)

---

## License

MIT License (add this in your `setup.py` if desired)

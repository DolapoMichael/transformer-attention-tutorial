# Transformer Attention Mechanisms — ML Tutorial

**Author:** Titiloye Dolapo Michael  
**Course:** Machine Learning  

> A practical tutorial on Scaled Dot-Product Attention and Multi-Head Attention, with a working sentiment analysis demo on the IMDB dataset.

## Overview

This repository contains the code and tutorial for a machine learning assignment exploring **Transformer Attention Mechanisms** — specifically:

- How Scaled Dot-Product Attention works (from scratch in NumPy)
- Why Multi-Head Attention outperforms single-head attention
- How to visualise attention weights on real text
- A full sentiment classifier trained on IMDB movie reviews

## Repository Structure

```
├── transformer_attention_tutorial.ipynb   # Main Jupyter notebook (runnable)
├── tutorial.html                          # Tutorial webpage
├── README.md
└── LICENSE
```

## How to Run

### Requirements

```bash
pip install torch torchtext matplotlib seaborn numpy pandas datasets
```

### Run the notebook

```bash
jupyter notebook transformer_attention_tutorial.ipynb
```

The notebook will:
1. Load the IMDB dataset automatically via HuggingFace `datasets`
2. Build and train a Transformer sentiment classifier
3. Generate all figures used in the tutorial
4. Produce attention weight visualisations on example reviews

> **Note:** Training takes ~5–10 minutes on CPU, or ~2 minutes on GPU. All figures are saved as `.png` files in the working directory.

## Key Results

| Model | Attention Heads | Test Accuracy |
|-------|----------------|---------------|
| Single-head | 1 | ~79–81% |
| Multi-head  | 4 | ~83–86% |
| Multi-head  | 8 | ~84–87% |

## References

1. Vaswani et al. (2017). *Attention is All You Need.* https://arxiv.org/abs/1706.03762
2. Alammar, J. (2018). *The Illustrated Transformer.* https://jalammar.github.io/illustrated-transformer/
3. Devlin et al. (2018). *BERT.* https://arxiv.org/abs/1810.04805
4. HuggingFace IMDB Dataset: https://huggingface.co/datasets/imdb

## Accessibility

- Colourblind-friendly plots (non-red/green primary colours for comparison charts)
- ARIA labels and semantic HTML in the tutorial webpage
- Alt-text provided for all figures in the notebook markdown cells

## License

MIT License — see [LICENSE](LICENSE) for details. You are free to use, modify, and distribute this code with attribution.

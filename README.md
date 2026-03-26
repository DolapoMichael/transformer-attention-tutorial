# Transformer Attention Mechanisms — ML Tutorial

**Author:** Titiloye Dolapo Michael  
**Course:** Machine Learning  
**GitHub:** https://github.com/DolapoMichael/transformer-attention-tutorial

> A practical tutorial on Scaled Dot-Product Attention and Multi-Head Attention, with a working implementation in pure NumPy and a sentiment analysis demo on the IMDB dataset.

## Overview

This repository contains the code and tutorial for a machine learning assignment exploring **Transformer Attention Mechanisms** — specifically:

- How Scaled Dot-Product Attention works (implemented from scratch in NumPy)
- Why Multi-Head Attention outperforms single-head attention
- How to visualise attention weights on real text
- A sentiment classifier trained on IMDB movie reviews using our attention implementation

## Repository Structure

```
├── transformer_attention_tutorial.ipynb   # Main Jupyter notebook (fully runnable)
├── Transformer Attention Mechanisms.pdf   # Tutorial PDF (submitted work)
├── README.md
└── LICENSE
```

## How to Run

### Requirements

```
pip install numpy matplotlib seaborn scikit-learn datasets
```

### Run the notebook

```
jupyter notebook transformer_attention_tutorial.ipynb
```

The notebook will:

1. Install all required packages automatically (first cell)
2. Build Scaled Dot-Product Attention from scratch in NumPy
3. Build Multi-Head Attention from scratch in NumPy
4. Load IMDB movie reviews and run a sentiment analysis demo
5. Generate all 7 figures used in the tutorial
6. Produce attention weight visualisations on real reviews

> **Note:** No GPU or deep learning framework required. The notebook runs on CPU using NumPy only and completes in under 2 minutes.

## Key Results

| Model | Attention Heads | Test Accuracy |
| --- | --- | --- |
| Single-head | 1 | ~79% |
| Multi-head | 2 | ~53% |
| Multi-head | 4 | ~54% |
| Multi-head | 8 | ~52% |

> Accuracy figures from the IMDB demo using logistic regression on attention-pooled embeddings.

## Figures Generated

| Figure | Description |
| --- | --- |
| fig1_rnn_vs_attention.png | RNN sequential flow vs attention direct connections |
| fig2_attention_steps.png | Step-by-step scaled dot-product attention heatmaps |
| fig3_multihead_attention.png | Four attention heads showing different patterns |
| fig4_positional_encoding.png | Sinusoidal positional encoding matrix |
| fig5_head_comparison.png | Single-head vs multi-head accuracy comparison |
| fig6_attention_on_reviews.png | Attention heatmaps on IMDB reviews |
| fig7_token_importance.png | Token importance via average attention received |

## References

1. Vaswani et al. (2017). *Attention is All You Need.* https://arxiv.org/abs/1706.03762
2. Alammar, J. (2018). *The Illustrated Transformer.* https://jalammar.github.io/illustrated-transformer/
3. Devlin et al. (2018). *BERT.* https://arxiv.org/abs/1810.04805
4. HuggingFace IMDB Dataset: https://huggingface.co/datasets/imdb
5. NumPy Documentation: https://numpy.org/doc/

## Accessibility

- Colourblind-friendly plots (blue/red palette, not red/green)
- Alt-text descriptions provided for all 7 figures in notebook markdown cells
- ARIA labels and semantic structure in tutorial HTML source

## License

MIT License — see [LICENSE](LICENSE) for details. You are free to use, modify, and distribute this code with attribution.

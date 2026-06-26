# Natural Language Processing (NLP)

Seq2seq recipe generation — learning to produce cooking steps from a list of ingredients, with six progressively more powerful architectures.

All notebooks are runnable in Google Colab with no local setup required.

## The Task

Given a set of ingredients (e.g., `chicken, garlic, lemon, olive oil`), generate a sequence of cooking steps. This is a sequence-to-sequence (encoder-decoder) problem trained on a cooking dataset.

## Notebooks — `recipe-generation-seq2seq/`

| Notebook | Architecture | Key Idea |
|---|---|---|
| [RNN Baseline](recipe-generation-seq2seq/seq2seq_rnn_baseline.ipynb) | Vanilla RNN enc-dec | Simplest possible seq2seq |
| [RNN + Attention](recipe-generation-seq2seq/seq2seq_rnn_with_attention.ipynb) | RNN + Bahdanau attention | Soft alignment over encoder states |
| [Attention Enc-Dec](recipe-generation-seq2seq/seq2seq_attention_encoder_decoder.ipynb) | Dedicated attention encoder | Specialised attention encoder architecture |
| [LSTM Enc-Dec](recipe-generation-seq2seq/seq2seq_lstm_encoder_decoder.ipynb) | Multi-layer LSTM | Gated memory for long-range dependencies |
| [Set Encoder + Coverage](recipe-generation-seq2seq/seq2seq_set_encoder_coverage.ipynb) | Order-invariant encoder | Coverage mechanism to reduce repetition |
| [Pointer-Generator](recipe-generation-seq2seq/seq2seq_pointer_generator.ipynb) | LSTM + pointer-generator | Copies ingredient tokens directly when needed |

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aryabhardwaj23/NATURAL-LANGUAGE-PROCESSING-NLP-/blob/main/recipe-generation-seq2seq/seq2seq_rnn_baseline.ipynb)

---

## Stack

Python · PyTorch · NumPy · Jupyter

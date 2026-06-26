<div align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=30&duration=2800&pause=2000&color=A855F7&center=true&vCenter=true&width=940&lines=Natural+Language+Processing+%F0%9F%A4%96;Seq2Seq+%7C+Attention+%7C+Transformers;Teaching+Machines+to+Cook+%F0%9F%A7%91%E2%80%8D%F0%9F%8D%B3" alt="Typing SVG" />
</div>

<div align="center">
  <img src="https://media.giphy.com/media/fwbZnTftCXVocKzfxR/giphy.gif" width="400"/>
</div>

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-red.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![Colab](https://img.shields.io/badge/Google-Colab-yellow.svg)

**Six progressively powerful seq2seq architectures — all trained to generate recipes from ingredients**

</div>

---

## 🍳 The Task

Given a list of ingredients → generate step-by-step cooking instructions.

This is a **sequence-to-sequence (encoder-decoder)** problem — the same family of models behind early machine translation systems. Six architectures are explored, increasing in complexity and capability.

```
Input:  ["chicken", "garlic", "lemon", "olive oil", "thyme"]
Output: "Heat olive oil in pan. Add garlic and cook until golden.
         Add chicken and brown on both sides. Squeeze lemon over
         the top, add thyme, and simmer for 15 minutes..."
```

---

## 📂 Projects — `recipe-generation-seq2seq/`

### 🏁 Baseline Models

<table>
<tr>
<td width="50%">

**RNN Baseline**

Vanilla RNN encoder-decoder — the simplest possible seq2seq. Sets the performance baseline with no attention.

**Architecture:** Encoder RNN → hidden state → Decoder RNN

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aryabhardwaj23/NATURAL-LANGUAGE-PROCESSING-NLP/blob/main/recipe-generation-seq2seq/seq2seq_rnn_baseline.ipynb)

</td>
<td width="50%">

**RNN + Attention**

Adds Bahdanau attention — the decoder learns *where* to look in the encoder output at each step.

**Architecture:** Encoder RNN → attention weights → context vector → Decoder

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aryabhardwaj23/NATURAL-LANGUAGE-PROCESSING-NLP/blob/main/recipe-generation-seq2seq/seq2seq_rnn_with_attention.ipynb)

</td>
</tr>
</table>

---

### ⚙️ Intermediate Models

<table>
<tr>
<td width="50%">

**Attention Encoder-Decoder**

Dedicated attention encoder (AttnEncoderRNN) — the encoder itself is attention-aware, not just the decoder.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aryabhardwaj23/NATURAL-LANGUAGE-PROCESSING-NLP/blob/main/recipe-generation-seq2seq/seq2seq_attention_encoder_decoder.ipynb)

</td>
<td width="50%">

**LSTM Encoder-Decoder**

Multi-layer LSTM — gated memory cells for better long-range dependency modelling.

**Key gain:** Remembers earlier ingredients when generating later steps.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aryabhardwaj23/NATURAL-LANGUAGE-PROCESSING-NLP/blob/main/recipe-generation-seq2seq/seq2seq_lstm_encoder_decoder.ipynb)

</td>
</tr>
</table>

---

### 🌶️ Advanced Models

<table>
<tr>
<td width="50%">

**Set Encoder + Coverage**

Order-invariant encoder (ingredients are a *set*, not a sequence) paired with a coverage mechanism that tracks which ingredients have been mentioned — reducing repetition.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aryabhardwaj23/NATURAL-LANGUAGE-PROCESSING-NLP/blob/main/recipe-generation-seq2seq/seq2seq_set_encoder_coverage.ipynb)

</td>
<td width="50%">

**Pointer-Generator Network**

LSTM encoder + pointer-generator decoder with coverage. Can *copy* ingredient tokens directly into the output — useful when ingredients appear verbatim in the recipe steps.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aryabhardwaj23/NATURAL-LANGUAGE-PROCESSING-NLP/blob/main/recipe-generation-seq2seq/seq2seq_pointer_generator.ipynb)

</td>
</tr>
</table>

---

## 📈 Architecture Progression

| Model | Attention | LSTM | Coverage | Pointer |
|---|:---:|:---:|:---:|:---:|
| RNN Baseline | ❌ | ❌ | ❌ | ❌ |
| RNN + Attention | ✅ | ❌ | ❌ | ❌ |
| Attention Enc-Dec | ✅ | ❌ | ❌ | ❌ |
| LSTM Enc-Dec | ✅ | ✅ | ❌ | ❌ |
| Set Encoder + Coverage | ✅ | ✅ | ✅ | ❌ |
| Pointer-Generator | ✅ | ✅ | ✅ | ✅ |

---

## 🛠️ Tech Stack

<div align="center">

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Google Colab](https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)

</div>

---

## 🚀 Run Locally

```bash
git clone https://github.com/aryabhardwaj23/NATURAL-LANGUAGE-PROCESSING-NLP.git
cd NATURAL-LANGUAGE-PROCESSING-NLP
pip install torch numpy pandas jupyter
jupyter notebook
```

The `recipe-generation-seq2seq/Cooking_Dataset.zip` contains the training data — unzip it before running any notebook.

---

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=17,20,24&height=100&section=footer"/>

  **⭐ Star this repo if the pointer-generator blew your mind!**

  ![Visitor Count](https://komarev.com/ghpvc/?username=aryabhardwaj23-nlp&color=blueviolet&style=for-the-badge&label=VISITORS)
</div>

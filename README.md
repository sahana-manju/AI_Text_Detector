# 🧠 AI Text Detector

## 🔍 Introduction

In recent times, the use of AI-generated content has exploded — from blog posts and essays to code and creative writing. As powerful as these tools are, there's a growing need to **distinguish between human-written and AI-generated text**. This project tackles that problem by building an **AI Text Detector** that can classify a piece of text as either AI- or human-generated.

---

## 📦 Dataset

The dataset used in this project was downloaded from Kaggle’s [LLM Detect AI-Generated Text Competition](https://www.kaggle.com/competitions/llm-detect-ai-generated-text/data). It contains a mix of AI- and human-written passages.

---

## 🧹 Preprocessing & Feature Engineering

To improve model performance, several structural and linguistic features were engineered:

- `text_length` – Total number of characters
- `mean_word_length` – Average word length
- `sentences` – Number of sentences
- `sentence_length` – Average length of a sentence
- `mean_sentence` – Mean sentence word count
- `unique_word_count` – Count of unique words
- `proper_noun_count` – Number of proper nouns
- `number_count` – Number of numeric tokens

Additionally, **common typos were replaced with the token `TYPO`**. This helped models learn that the presence of typos strongly correlates with human-written text, as AI-generated text tends to be grammatically cleaner.

---

## 🤖 Models Used

Multiple models were trained and evaluated using **3-fold cross-validation**:

| Model                    | Accuracy |
|--------------------------|----------|
| Multinomial Naive Bayes  | 70%      |
| Random Forest            | 88%      |
| XGBoost                  | 85%      |
| **BERT** (Transformer)   | **99%**  |

BERT significantly outperformed traditional machine learning models by leveraging deep contextual understanding of language.

---

## ✅ Conclusion

The project demonstrates that combining classic NLP features (like typo detection and word counts) with advanced models like BERT can effectively distinguish AI-generated content from human-written text. BERT’s 99% accuracy highlights the power of transformers in understanding nuanced language patterns, especially when enhanced with thoughtful preprocessing.

---



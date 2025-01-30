# Sentiment Analysis in Earnings Call Transcripts & Stock Price Impact

## Project Overview
This repository contains research and analysis related to sentiment extraction from **earnings call transcripts** and its impact on **stock price movements**. The project started as a **group assignment**, where we explored sentiment differences in **Prepared Remarks vs. Q&A sections** of earnings call transcripts. Building upon this, I extended the research individually by integrating **stock price data** to analyze how sentiment influences market movements.

---

## Files and Structure

### Group Project Files:
- 📄 **REPORT-13.pdf** – Detailed research report on sentiment analysis in earnings call transcripts.
- 📊 **PRESENTATION-13.pdf** – Presentation summarizing the findings.
- 📜 **CODE-13.ipynb** – Jupyter Notebook with sentiment analysis code.

### Individual Analysis Files:
- 📄 **Untitled presentation.pdf** – Stock price impact analysis.
- 📜 **ai_project1.ipynb** – Notebook performing sentiment-based stock prediction.

---

## Group Research: Sentiment in Earnings Call Transcripts

### 🔎 Research Question
**Which sections of earnings call transcripts (Prepared Remarks vs. Q&A) provide stronger financial sentiment signals?**

### 🛠️ Methodology
- **Data:** 18,755 earnings call transcripts from Motley Fool.
- **Preprocessing:** TF-IDF, Named Entity Recognition (NER), Latent Dirichlet Allocation (LDA).
- **Sentiment Analysis:** Using **FinBERT**, a pre-trained financial NLP model.
- **Key Approaches:**
  - **Sliding Window Technique** to handle long transcripts.
  - **Stop-word removal comparison** (with/without English stop words).

### 📊 Findings
- **Prepared Remarks** carry **stronger sentiment signals**.
- **Q&A sessions** are more **neutral** and provide less financial sentiment impact.
- Removing stop-words speeds up computation **3× faster**, but weakens the sentiment signal.

---

## Individual Research: Sentiment & Stock Price Impact

### 🔎 Goal
To investigate **how sentiment extracted from earnings call transcripts influences stock price movements**.

### 🛠️ Methodology
- **Stock Data:** Retrieved from Yahoo Finance API.
- **Feature Engineering:**
  - Stock prices **10-30 days before** transcript release.
  - Stock prices **3 days after** release.
  - **Macroeconomic factors** (COVID, U.S. Presidential Elections).
- **Models Used:**
  - Traditional ML: **Random Forest, Logistic Regression, XGBoost**
  - Deep Learning: **LSTM, GRU, CNN, RNN, CNN+RNN**

### 📊 Results
- **Sentiment influences stock movement, but impact is modest.**
- **Best accuracy:** CNN+RNN model with **76% accuracy**.
- **Sentiment scores improve performance**, but removing macroeconomic factors (COVID/elections) gave better results.
- **No significant relationship between COVID & stock direction**, but **higher positive sentiment was correlated with stock increases**.

### 🔬 Future Research
- Use **FinnHub API** to collect **more stock data**.
- **Scale analysis** to a larger dataset for robustness.
- Explore **longer-term stock price effects** beyond 3 days.

---


## 📌 Conclusion
This research contributes to understanding **how financial sentiment impacts markets** and highlights the **importance of distinguishing between different transcript sections**. The individual project further demonstrates how **sentiment features enhance predictive stock price models**, providing insights for future research and real-world applications.



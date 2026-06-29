# 🧠 App Review Sentiment Analyzer

An end-to-end Natural Language Processing project that classifies user reviews as
**Positive**, **Neutral**, or **Negative** using a **TF-IDF** vectorizer and a
**Linear SVM** classifier, wrapped in an interactive **Streamlit** dashboard.

> Universiti Teknologi Malaysia · Faculty of Artificial Intelligence

---

## ✨ Features

The dashboard has five pages:

1. **Home** — project overview, team, and instructions
2. **Sentiment Analyzer** — paste a review and get a live prediction with a
   confidence score and word-importance highlighting
3. **Data Explorer** — browse the dataset, statistics, and label distribution
4. **Visualizations** — Word Cloud, Class Distribution, Confusion Matrix,
   Model Comparison, and Top 20 Words
5. **Model Information** — preprocessing, TF-IDF, the model, and live
   Accuracy / Precision / Recall / F1 scores

Input text is cleaned with the **same 7-step pipeline used during training**
(lowercase → remove URLs → remove punctuation → remove numbers → tokenize →
remove stopwords → lemmatize) so predictions match training conditions.

---

## 🚀 Setup & Run Locally

```bash
# 1. Clone the repo
git clone https://github.com/OsamaMonzer/Nlp.git
cd Nlp

# 2. (Optional) Create a virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Launch the app
streamlit run app.py
```

Then open `http://localhost:8501` in your browser.  
The first run downloads NLTK data automatically — keep your internet on.

---

## 📁 Project Structure

```
.
├── app.py                        # Main Streamlit application (5 pages)
├── requirements.txt              # Python dependencies
├── README.md                     # Setup and usage instructions
├── .gitignore                    # Ignore large/generated files
│
├── data/
│   └── cleaned_dataset.csv       # Preprocessed Google Play reviews dataset
│
├── models/
│   ├── spam_model.pkl            # Trained Linear SVM model (joblib)
│   └── vectorizer.pkl            # Fitted TF-IDF vectorizer
│
├── notebooks/
│   └── NLP_PROJECT.ipynb         # Model development & experimentation
│
└── .streamlit/
    └── config.toml               # Streamlit theme configuration
```

> Note: `spam_model.pkl` is named for historical reasons — the actual task is **sentiment analysis**.

---

## 👥 Team

| Member  | Role                                        |
|---------|---------------------------------------------|
| Ahmed   | Data Preprocessing & Feature Engineering   |
| Osama   | Model Training & Evaluation                |
| Abobakr | Streamlit App & Visualization              |

---

## 🛠️ Tech Stack

Python · scikit-learn · NLTK · pandas · NumPy · Plotly · WordCloud · Streamlit

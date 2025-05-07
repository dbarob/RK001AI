# RK001AI: Starter AI Projects for Local ML Work

This repository contains three small, standalone AI/ML projects designed to be run locally for experimentation, learning, or real-world data tasks.

## 📦 Project Structure

```
RK001AI/
├── 01-attrition-prediction/
│   └── attrition_model.ipynb
├── 02-sentiment-analysis/
│   └── sentiment_analysis.ipynb
├── 03-anomaly-detection/
│   └── anomaly_detection.ipynb
├── requirements.txt
├── SETUP.md
└── README.md
```

---

## 📘 Project Summaries

### 1. Employee Attrition Prediction

* **Goal**: Predict whether an employee is likely to leave using HR data.
* **Tech**: `pandas`, `scikit-learn`
* **Model**: Random Forest
* **Dataset**: IBM HR Analytics (download separately)

### 2. Sentiment Analysis

* **Goal**: Detect sentiment (positive/negative) from open-text feedback.
* **Tech**: `transformers`, `torch`
* **Model**: Pretrained DistilBERT from Hugging Face

### 3. Anomaly Detection

* **Goal**: Identify unusual patterns in tabular numerical data.
* **Tech**: `pyod`, `matplotlib`
* **Model**: Isolation Forest

---

## ⚙️ Setup Instructions

See [`SETUP.md`](./SETUP.md) for full instructions.

Basic steps:

```bash
# Optional: create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install all required packages
pip install -r requirements.txt

# (Optional) Launch Jupyter Notebook
jupyter notebook
```

To register the kernel for Jupyter:

```bash
pip install ipykernel
python -m ipykernel install --user --name ai_env --display-name "Python (ai_env)"
```

---

## 🧠 AI Workflow Diagram

```mermaid
graph TD
  A[CSV Data Input] --> B[Preprocessing with Pandas]
  B --> C[Train/Test Split]
  C --> D[Train ML Model (RandomForest, etc.)]
  D --> E[Model Predictions]
  E --> F[Evaluation (Classification Report)]
```

---

## ✍️ License

MIT License — use freely and modify as needed.

---

## 🙋 Need Help?

Open an issue or pull request on GitHub, or reach out to the project maintainer.

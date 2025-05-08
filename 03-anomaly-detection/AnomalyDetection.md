# 📈 Understanding Anomaly Detection with Isolation Forest

This document explains how the anomaly detection model works with your data, how to read the results (including the scatter plot), and how this applies to real-world council data (e.g. Granicus).

---

## 🧾 What the Model Does with Your CSV Data

1. You load a CSV with two numeric columns (e.g., `Feature1`, `Feature2`).
2. Each row becomes a point in space (X, Y).
3. The model learns what “normal” data looks like.
4. It flags anything that looks too different as an **anomaly**.

### 🔍 Simple Analogy:

Imagine 100 people wearing grey and 5 wearing red suits. The model spots the red suits as anomalies — because they’re easy to separate.

---

## 📊 What the Scatter Plot Shows

### Axes:

* **X-axis**: `Feature1`
* **Y-axis**: `Feature2`

Each point represents one row from your dataset.

---

## 🎯 Color = AI Prediction

The Isolation Forest model labels each point:

* `0` = **Normal** (blue)
* `1` = **Anomaly** (red)

```python
plt.scatter(X[:, 0], X[:, 1], c=outliers, cmap='coolwarm')
```

---

## 🔍 How to Interpret It

* **Blue cluster** = Normal data
* **Red dots** = Outliers

If your CSV has 95 values near (0, 0) and 5 near (6, 6):

* Blue points form a cloud near the origin
* Red points will sit far away — they’re flagged as unusual

---

## ✅ Why It Matters

* Makes anomalies visible
* Helps explain model behavior
* Supports data cleaning, alerting, and insights

---

## 🖼 Visual Guide

This image shows how data flows from a CSV into the model and how results are visualized.

---

## 🏛 Use Cases for UK Council Data (e.g. Granicus)

Anomaly detection is useful for spotting outliers in council service data.

### Form Submissions:

* Time to complete
* Number of edits
* Submissions at odd hours (e.g. 2am)

> Identify suspicious or broken interactions.

### Resident Usage Patterns:

* Unusually high service request counts
* Rare or unexpected combinations

> Spot unusual users or automated activity.

### Web or System Logs:

* Usage spikes
* Drop-offs
* Uncommon device/browser usage

> Detect journey failures or technical issues.

### To Use This:

* Convert your form/system data to numbers
* Run Isolation Forest
* Investigate anything flagged as an anomaly

---

## 💡 Tip

Save predictions with labels (0 or 1) back into a CSV. That way, you can trace each red dot on the plot to the exact row in your original data.

# 📉 Understanding Attrition Prediction with Random Forest

This document explains how the attrition prediction model works, how to interpret the results, and how it applies to real-world UK council datasets like Liquid Logic and Synergy.

---

## 🧠 What the Model Does

You’re using a **Random Forest Classifier**, a supervised AI model that learns from past cases where you already know who left and who stayed.

### How it works:

1. It looks at patterns in employee or service user data.
2. It learns which combinations of factors lead to people leaving.
3. It predicts whether new or current people are at risk of leaving.

---

## 📊 Example Model Output

```
              precision    recall  f1-score   support

           0       0.88      0.95      0.91       246
           1       0.75      0.53      0.62        54

    accuracy                           0.86       300
```

* **Class 0** = Stayed
* **Class 1** = Left
* **Precision (class 1)** = 0.75 → When the model predicts someone will leave, it’s right 75% of the time.
* **Recall (class 1)** = 0.53 → It catches 53% of all people who actually left.
* **Accuracy** = 86% overall predictions correct.

---

## 🏛 Real-World UK Council Use Cases

### 🧑‍⚕️ Staff Retention in Social Care (Liquid Logic)

* Data: Staff role, tenure, caseloads, region, training history
* Goal: Predict who is at risk of leaving so HR can intervene

### 🏡 Foster Carer Attrition (Liquid Logic)

* Data: Carer age, recent placements, support hours, event logs
* Goal: Identify carers at risk of dropping out

### 🎓 Pupil NEET Risk Detection (Synergy)

* Data: Attendance, behaviour, support plans, postcode history
* Goal: Predict risk of disengagement or NEET classification

---

## ✅ How to Use This

1. Prepare historical data where outcomes are known (e.g., "left" = yes/no)
2. Train the model on features (age, location, frequency, etc.)
3. Use the model to score new or current people
4. Act on high-risk predictions with outreach or support

---

## 💬 Tip

Even if accuracy is high, always check recall for the "leave" class — catching those early is the real value of predictive attrition models.

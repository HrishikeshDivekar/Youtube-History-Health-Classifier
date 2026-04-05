---

# 🎯 YouTube Watch History — Health Classifier

A data-driven machine learning project that analyzes your YouTube watch history and classifies content into **“Healthy / Productive”** vs **“Brainrot / Mindless”** categories.

This project helps you **quantify your digital consumption habits**, identify patterns, and make better decisions about your screen time.

---

## 🚀 Overview

This notebook-based pipeline processes raw YouTube watch history (JSON), applies **rule-based labeling + machine learning**, and generates:

* 📊 Behavioral insights
* 🧠 Content quality classification
* 📈 Visual analytics dashboards
* 💾 Exportable datasets & trained model

---

## 🧩 Key Features

* ✅ JSON watch history parsing & cleaning
* 🏷️ Rule-based auto-labeling using keyword heuristics
* 🤖 ML-based classification (text-based model)
* 📊 Health score computation
* 📈 Rich visualizations (daily trends, heatmaps, distributions)
* 🔎 Real-time classification for new videos
* 💾 Exportable results + trained model

---

## 🏗️ Project Pipeline

1. **Data Ingestion**

   * Input: YouTube `watch-history.json`
   * Parsed into structured dataframe

2. **Data Cleaning & Feature Engineering**

   * Extract:

     * Title
     * Channel
     * Timestamp
     * Hour / Day
     * Shorts detection

3. **Rule-Based Labeling**

   * Uses keyword lists:

     * `HEALTHY_KEYWORDS`
     * `BRAINROT_KEYWORDS`
   * Generates initial labels

4. **Machine Learning Model**

   * Text vectorization (likely TF-IDF)
   * Binary classification:

     * `0 → Healthy`
     * `1 → Brainrot`

5. **Evaluation & Prediction**

   * Train/test split
   * Probability-based prediction

6. **Visualization Layer**

   * Health score
   * Daily trends
   * Hourly heatmaps
   * Pie charts & distributions

7. **Export & Deployment**

   * CSV export
   * Saved ML model
   * Function to classify new videos

---

## 📊 Example Outputs

* 🟢 % Healthy vs 🔴 Brainrot consumption
* 📅 Daily “brainrot probability” trends
* 🕒 Time-of-day consumption heatmap
* 📉 Behavioral patterns over time

---

## 🧠 Real-Life Use Cases

### 👨‍🎓 Students

* Track whether YouTube usage is **educational or distracting**
* Improve study discipline

### 💼 Professionals

* Identify productivity leaks in daily routine
* Optimize learning vs entertainment balance

### 📱 Digital Wellbeing

* Build awareness of **content consumption habits**
* Reduce mindless scrolling

### 👨‍👩‍👧 Parents

* Monitor children's viewing patterns
* Encourage healthier content consumption

### 🧑‍💻 Self-Improvement Enthusiasts

* Quantify “dopamine vs growth” content ratio
* Align media habits with personal goals

---

## ⚙️ Technical Specifications

### 🧰 Technologies Used

* **Language:** Python 3.x
* **Notebook:** Jupyter Notebook
* **Libraries:**

  * `pandas`, `numpy` — data processing
  * `matplotlib`, `seaborn`, `plotly` — visualization
  * `scikit-learn` — ML pipeline
  * `wordcloud` — text visualization

---

### 🤖 Machine Learning Details

* **Problem Type:** Binary Text Classification

* **Input:** Video title + channel name

* **Output:**

  * Class label (Healthy / Brainrot)
  * Probability score

* **Pipeline Components:**

  * Text preprocessing
  * Vectorization (TF-IDF or similar)
  * Classifier (e.g., Logistic Regression / Naive Bayes)

---

### 📁 Input / Output

#### Input

```bash
watch-history.json
```

#### Output

```bash
youtube_classified.csv
model.pkl (or similar)
```

---

## ▶️ How to Run

1. Export your YouTube watch history:

   * Google Takeout → YouTube → History

2. Place file:

```bash
watch-history.json
```

3. Run notebook cells sequentially:

```bash
youtube_health_classifier.ipynb
```

4. View:

* Visualizations
* Health score
* Exported dataset

---

## 🔎 Classifying New Videos

Use the built-in function:

```python
classify_new("How to learn Python in 30 days", "Programming Channel")
```

Output:

* Prediction (Healthy / Brainrot)
* Probability score

---

## 📈 Feasibility & Impact

### ✔️ Feasibility

* Requires only:

  * Personal watch history
  * Standard Python environment
* No external APIs needed
* Runs locally → privacy-friendly

### 📊 Accuracy Considerations

* Depends on:

  * Keyword quality
  * Training data size
* Hybrid approach (rules + ML) improves robustness

### ⚠️ Limitations

* Titles may not fully reflect content quality
* Cultural/contextual bias in keyword lists
* Binary classification oversimplifies content spectrum

---

## 🔮 Future Development Scope

### 🧠 Model Improvements

* Deep learning (BERT / transformers)
* Multilingual support
* Context-aware classification

### 🎯 Personalization

* User-specific labeling preferences
* Adaptive learning from feedback

### 🌐 Integration

* Browser extension for live tracking
* YouTube API integration
* Real-time dashboard

### 📊 Advanced Analytics

* Addiction pattern detection
* Dopamine scoring system
* Weekly/monthly reports

### 📱 Productization

* Mobile app for digital wellbeing
* Gamified productivity tracking

---

## 🛡️ Ethical Considerations

* Designed for **self-awareness, not judgment**
* No external data sharing required
* Fully local and privacy-conscious

---

## 🤝 Contributing

Contributions are welcome! Possible areas:

* Better keyword datasets
* Improved ML models
* UI/dashboard enhancements

---

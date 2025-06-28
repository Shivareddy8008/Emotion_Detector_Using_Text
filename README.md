# Emotion_Detector_Using_Text
# 💬 Emotion Detection from Text using NLP & Machine Learning

A machine learning project that classifies textual input (such as comments, reviews, or sentences) into **emotion categories** like *joy, sadness, anger, fear, love,* and *surprise*. Built using **Natural Language Processing (NLP)** techniques and a **Logistic Regression** classifier, and deployed with a **Gradio interface** for real-time emotion detection.

---

## 📁 Dataset

- **File Name**: `training.csv`
- **Size**: 5170+ text entries
- **Columns**:
  - `text`: Raw textual data (e.g., messages, tweets)
  - `label`: Emotion label (e.g., sadness, joy)
  - `label_num`: Numeric label (0–5)

---

## ⚙️ Features & Workflow

1. **Text Preprocessing**:
   - Lowercasing
   - Tokenization using NLTK
   - Stopword removal
   - Removal of punctuation and digits

2. **Feature Extraction**:
   - Applied **TF-IDF Vectorization** (`max_features=5000`) to convert cleaned text into numerical features

3. **Model Training**:
   - Used **Logistic Regression** (`max_iter=1000`)
   - Data split: 75% training, 25% testing

4. **Model Evaluation**:
   - Evaluated using `classification_report` with precision, recall, and F1-score per emotion class

5. **Deployment**:
   - Created an interactive **Gradio interface** to detect emotion from live user input

---

## 🎯 Emotion Categories

| Label Number | Emotion   |
|--------------|-----------|
| 0            | Sadness   |
| 1            | Joy       |
| 2            | Love      |
| 3            | Anger     |
| 4            | Fear      |
| 5            | Surprise  |

---

## 🖥️ Gradio Web Interface

Users can input any sentence, and the model returns the predicted **emotion** label.

### Sample Output:
> Input: *"I can't believe you did this!"*  
> Output: **Emotion: Surprise**

---

## 🚀 How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/emotion-detector.git
cd emotion-detector

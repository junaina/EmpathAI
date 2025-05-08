# 🧠 EmpathAI: An Emotion-Aware Motivational Assistant with Mood Tracker

EmpathAI is a simple emotional AI assistant that detects emotions from text and responds with motivational messages. It also logs user moods over time for trend analysis.

## 🚀 Project Goals
- Learn how to train and fine-tune a transformer-based model (BERT)
- Detect basic emotions from text (joy, anger, fear, love, surprise)
- Respond in a human-like, comforting way
- Track emotional trends over time

---

## 📂 Features
- Emotion classification using **BERT** (fine-tuned on GoEmotions)
- Paragraph-level analysis: detects emotions sentence by sentence
- Dominant emotion detection with a relevant motivational response
- Mood logging to a `.csv` file with timestamps
- Trend visualization using matplotlib

---

## 🧰 Tech Stack
- **Python 3** (Google Colab)
- **HuggingFace Transformers**
- **TensorFlow + Keras**
- **Pandas / Matplotlib / NLTK**
- Dataset: [GoEmotions](https://github.com/google-research/goemotions)

---

## ⚙️ How It Works

1. **Preprocessing**:
   - Loads the GoEmotions dataset
   - Maps 28 emotions to 5 core ones
   - Encodes labels

2. **Model**:
   - Loads pre-trained BERT
   - Fine-tunes it on our 5-class emotion task

3. **Prediction**:
   - Tokenizes new text inputs
   - Predicts sentence-wise emotion
   - Finds dominant emotion
   - Responds with a motivational message

4. **Logging**:
   - Saves input, emotion, and response to `mood_tracker_log.csv`
   - Can visualize emotion trends over time

---

## 🧪 Example Usage

```python
paragraph = "I feel exhausted and anxious. But my friends give me hope."
analyze_paragraph(paragraph)

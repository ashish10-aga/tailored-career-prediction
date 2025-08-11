# 🎯 Tailored Career Prediction Based on Emotional & Personality Traits

This project predicts suitable career roles for an individual based on their personality profile and emotional traits using the **Big Five Personality Model (OCEAN)**.  
The model takes in personality scores or processes a short video interview to extract traits, then predicts multiple career options.

---

## 📌 Overview
The system uses:
- **Machine Learning** (Random Forest, SVM, KMeans, KNN)
- **Video & Audio Processing** (extract personality cues from speech and facial expressions)
- **Multi-label classification** to recommend more than one career if applicable

---

## 📂 Dataset
**Note:** The dataset is **not included** in this repository for privacy reasons.

**How it was created:**
- Collected 409+ interview videos from public sources (e.g., YouTube).
- Trimmed videos to show only the person speaking.
- Three annotators scored each person on the Big Five personality traits:
  - Openness
  - Conscientiousness
  - Extraversion
  - Agreeableness
  - Neuroticism
- Annotators discussed disagreements until consensus was reached.
- Mapped personality profiles to one or more suitable career roles.
- Stored data in a CSV file (`merged_big5_scores.csv`) with the following columns:
  ```
  Video_ID, Openness, Conscientiousness, Extraversion, Agreeableness, Neuroticism, Career Role
  ```
- This CSV was used to train, validate, and test the ML models.

You can replicate this dataset creation process or adapt it with your own video data.

---

## ✨ Features
- 📹 **Video-based personality analysis**
- 🧠 **Machine Learning prediction models** (Random Forest, KMeans, SVM, KNN)
- 📊 **Multi-label classification** for multiple career suggestions
- 🖥 **Jupyter Notebook & Python script** implementations
- 🔍 Optional integration with **DeepFace** for facial emotion recognition
- ⚡ Predictions in under 5 minutes per video

---

## 🛠 Tech Stack
**Languages:** Python 3.8+  
**Libraries & Frameworks:**
- `pandas`, `numpy`, `scikit-learn`, `seaborn`, `matplotlib`
- `joblib` (model saving/loading)
- `moviepy`, `SpeechRecognition` (audio/video processing)
- `deepface` (emotion detection)
- `ipywidgets` (video upload in Jupyter)

---

## 📦 Installation
```bash
# Clone the repository
git clone https://github.com/ashish10-aga/tailored-career-prediction.git
cd tailored-career-prediction

# Create a virtual environment (optional)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

---

## 🚀 Usage

### **1️⃣ Running via Python script**
```bash
python model_train.py
```
Ensure you have a CSV in the same format as described in the **Dataset** section.

### **2️⃣ Running via Jupyter Notebook**
```bash
jupyter notebook model_train_video.ipynb
```
Upload a video through the provided widget to get predictions.

---

## 📂 Project Structure
```
personality-model/
│-- model_train.py              # Main ML pipeline script
│-- model_train_video.ipynb     # Notebook with video upload & prediction
│-- requirements.txt            # Dependencies
│-- README.md                   # Project documentation
│-- .gitignore                  # Files to ignore in Git
```

---

## 📊 Example Prediction
**Input Traits:**  
`Openness=3.5, Conscientiousness=4.0, Extraversion=3.2, Agreeableness=4.1, Neuroticism=2.5`

**Predicted Careers:**  
`['Data Analyst', 'Business Analyst', 'Project Manager']`

---

## 📈 Results
- **Random Forest Accuracy:** ~84%  
- **KMeans Clustering:** Groups candidates into 4 clusters mapped to career roles
- **Multi-label Classification:** Supports multiple job predictions per individual

---

## 📌 Future Work
- Deploy as a **web or mobile app**
- Add **multilingual support**
- Expand dataset for more diverse career coverage
- Improve accuracy with **deep learning models**

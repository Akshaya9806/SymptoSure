# 🩺 SYMPTOSURE – Smart Symptom Severity & Care Assistant

## 📌 Overview

SYMPTOSURE is an AI-powered healthcare assistance system that predicts diseases from user symptoms using Machine Learning. The system accepts symptoms through text and voice input, performs symptom analysis, predicts possible diseases, classifies severity levels, detects emergency conditions, and provides healthcare guidance.

The project integrates Machine Learning, FastAPI, MongoDB, multilingual processing, and speech technologies to deliver real-time healthcare assistance.

---

## 🚀 Features

- Disease prediction using Machine Learning
- Symptom analysis and preprocessing
- Text and Voice-based symptom input
- Multilingual support
- Severity classification (Low / Medium / High)
- Emergency (Red-Flag) symptom detection
- Healthcare guidance and precautions
- Suggested medical tests
- OTC recommendation support
- User authentication
- Health report generation
- Prediction history tracking
- MongoDB integration
- REST API architecture using FastAPI

---

## 🏗️ System Workflow

```text
User Input (Text / Voice)
          │
          ▼
Symptom Extraction & Mapping
          │
          ▼
Feature Engineering
(MultiLabelBinarizer)
          │
          ▼
Random Forest Model
          │
          ▼
Disease Prediction
          │
          ▼
Severity Classification
          │
          ▼
Emergency Detection
          │
          ▼
Healthcare Guidance
          │
          ▼
Report Generation
          │
          ▼
MongoDB Storage
```

---

## 🛠️ Technologies Used

### Backend
- FastAPI
- Python

### Machine Learning
- Scikit-Learn
- Random Forest Classifier

### Database
- MongoDB
- PyMongo

### Data Processing
- Pandas
- NumPy

### Visualization
- Matplotlib
- Seaborn

### Language & Speech Processing
- SpeechRecognition
- gTTS
- deep-translator

### Model Persistence
- Joblib

---

## 🤖 Machine Learning Workflow

### Data Preprocessing
- Missing value handling
- Symptom extraction and mapping
- MultiLabelBinarizer for feature encoding
- Label Encoding for disease labels

### Model Training
- Random Forest Classifier
- 80:20 Train-Test Split
- Noise injection for robustness testing

### Model Evaluation
- Accuracy Score
- Precision
- Recall
- F1 Score
- Confusion Matrix
- 5-Fold Cross Validation

---

## 📊 Model Performance

| Metric | Value |
|----------|----------|
| Test Accuracy | 84.04% |
| Cross Validation Accuracy | 90.42% |
| Diseases Covered | 41 |
| Symptoms Supported | 131 |

---

## 📂 Project Structure

```text
Symptosure/
│
├── api.py
├── predictor.py
├── train_model.py
├── evaluate_model.py
├── feature_engineer.py
├── data_prep.py
│
├── symptom_extractor.py
├── symptom_mapping.py
├── translator.py
├── stt_tts.py
│
├── severity.py
├── emergency.py
├── disease_matcher.py
│
├── database.py
│
├── dataset.csv
├── symptom_Description.csv
├── symptom_precaution.csv
├── disease_tests.csv
│
├── artifacts/
│   ├── model.joblib
│   ├── mlb.joblib
│   └── label_encoder.joblib
│
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

### Clone Repository

```bash
git clone https://github.com/your-username/symptosure.git
cd symptosure
```

### Create Virtual Environment

```bash
python -m venv venv
```

### Activate Virtual Environment

**Windows**

```bash
venv\Scripts\activate
```

**Linux / Mac**

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Run the Project

Start the FastAPI server:

```bash
uvicorn api:app --reload
```

Open:

```text
http://127.0.0.1:8000/docs
```

to access the Swagger API documentation.

---

## 🗄️ Database

MongoDB is used for:

- User Authentication
- Prediction History
- Generated Reports
- User Data Management

Default MongoDB Connection:

```text
mongodb://localhost:27017
```

---

## 🔍 Research Gap Addressed

Existing healthcare prediction systems mainly focus on disease prediction and often lack:

- Severity classification
- Emergency symptom detection
- Multilingual support
- Voice-based interaction
- Healthcare guidance
- Report generation
- Prediction history tracking

SYMPTOSURE addresses these limitations by integrating all these functionalities into a single AI-powered healthcare assistance platform.

---

## 🚀 Future Enhancements

- Deep Learning-based prediction models
- Mobile application support
- Doctor consultation integration
- Hospital recommendation system
- Wearable device integration
- Advanced NLP capabilities


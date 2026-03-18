# 💳 Customer Retention Intelligence System

An end-to-end Machine Learning system designed to predict customer churn with business-driven decision making using optimized threshold tuning.
This project combines **Machine Learning, Backend APIs, and Frontend UI** into a production-ready pipeline.

---

## 🚀 Live Demo

* 🔗 **API (FastAPI Docs):** https://churn-prediction-ml-app-jedn.onrender.com/docs
* 🎯 **Prediction Endpoint:** https://churn-prediction-ml-app-jedn.onrender.com/predict
* 🌐 **Frontend (Streamlit):** *(Add your Streamlit link here)*

---

## 📊 Key Features

* 📈 Predicts customer churn probability (not just binary output)
* 🎯 Uses **optimized decision threshold** instead of default 0.5
* ⚡ Real-time predictions via FastAPI backend
* 🖥️ Interactive Streamlit dashboard
* 🧠 Business-focused decision logic for churn prevention
* 🔍 Returns probability + threshold + prediction

---

## 🧠 Machine Learning Highlights

* **ROC-AUC Score:** 0.86 (strong classification performance)
* **Recall improved:** 44% → 75% using threshold optimization
* **Focus:** Reduce false negatives (high-risk customers missed)
* Model trained using structured customer data (banking domain)

---

## 🧩 System Architecture

```text
User Input (Streamlit UI)
        ↓
FastAPI Backend (Render)
        ↓
ML Model (Scikit-learn)
        ↓
Probability Output
        ↓
Threshold Decision Logic
        ↓
Final Prediction + Risk Insight
```

* Streamlit handles user interaction
* FastAPI serves predictions
* ML model outputs probability
* Custom threshold converts probability → decision

---

## 📡 API Usage

### 🔹 Endpoint

```http
POST /predict
```

### 🔹 Request Example

```json
{
  "CreditScore": 650,
  "Geography": "France",
  "Gender": "Male",
  "Age": 35,
  "Tenure": 5,
  "Balance": 50000,
  "NumOfProducts": 2,
  "HasCrCard": 1,
  "IsActiveMember": 1,
  "EstimatedSalary": 60000
}
```

### 🔹 Response Example

```json
{
  "prediction": 0,
  "churn_probability": 0.089,
  "threshold_used": 0.434
}
```

---

## ⚙️ Tech Stack

* **Language:** Python
* **Machine Learning:** Scikit-learn
* **Backend:** FastAPI
* **Frontend:** Streamlit
* **Libraries:** Pandas, NumPy, Joblib
* **Deployment:** Render

---

## ⚙️ How It Works

1. User enters customer details via UI
2. Data is sent to FastAPI backend
3. Model processes input and calculates probability
4. Custom threshold is applied
5. Final prediction + risk insights returned

---

## ▶️ Run Locally (Development Setup)

### 1️⃣ Clone repository

```bash
git clone https://github.com/Ir-Akst/churn-prediction-ml-app.git
cd churn-prediction-ml-app
```

### 2️⃣ Create virtual environment

```bash
python -m venv venv
venv\Scripts\activate   # Windows
```

### 3️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Run FastAPI backend

```bash
uvicorn api.main:app --reload
```

### 5️⃣ Run Streamlit frontend

```bash
streamlit run app/streamlit_app.py
```

---

## ⚠️ Important Notes

* Ensure model files are present in `/models` directory
* Use consistent library versions to avoid compatibility issues
* API uses **custom threshold (0.434)** for decision making

---

## 🔮 Future Improvements

* 🔍 Add SHAP-based explainability (feature importance)
* 🗄️ Store predictions in database
* 🔐 Add authentication system
* 🐳 Dockerize application
* 🔄 CI/CD pipeline for automated deployment
* 📊 Real-time monitoring and logging

---

## 🧠 Key Learning Outcomes

* Built full-stack ML system (Model → API → UI → Deployment)
* Understood precision-recall tradeoff and threshold tuning
* Solved real-world deployment challenges (versioning, paths, APIs)
* Implemented business-focused ML decision logic

---

## 👨‍💻 Author

**Akshat**
AI/ML & Data Science Enthusiast

---

## ⭐ If you like this project

Give it a ⭐ on GitHub and share your feedback!

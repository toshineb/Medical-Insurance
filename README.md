# 📊 Medical Insurance Cost Prediction using Machine Learning

## 📌 Project Overview
This project aims to predict **medical insurance charges** based on key factors such as **age, BMI, number of children, smoking status, gender, and region**. By leveraging various machine learning models, the project provides **insights into the primary cost drivers** and helps insurance providers make informed pricing and risk assessment decisions.

---

## 🔍 Key Findings
- 🚬 **Smoking status is the most significant factor** affecting insurance costs, significantly increasing charges.
- 📈 **Age and BMI have a strong positive correlation** with higher insurance costs.
- 📊 **Linear Regression achieved an R² score of 0.75**, explaining 75% of the variance in medical costs.
- 🌳 **Random Forest and XGBoost performed better**, with R² scores of **0.82 and 0.86** respectively on test data.
- ⚖ **Feature importance analysis confirmed that smoking, age, and BMI are the top predictors of medical insurance costs.**

---

## 📁 Dataset Information
The dataset consists of **1,338 records** with the following features:

| Column      | Description |
|------------|-------------|
| `age`      | Age of the insured person |
| `sex`      | Gender (`male` or `female`) |
| `bmi`      | Body Mass Index (BMI) |
| `children` | Number of children covered by insurance |
| `smoker`   | Whether the insured is a smoker (`yes` or `no`) |
| `region`   | Region of the insured (`northeast`, `northwest`, `southeast`, `southwest`) |
| `charges`  | Medical insurance charges (target variable) |

---

## 🛠 Technologies Used
### 📌 Python Libraries:
- **Pandas** – Data manipulation and preprocessing  
- **NumPy** – Numerical operations  
- **Matplotlib & Seaborn** – Data visualization  
- **Scikit-Learn** – Machine learning models and evaluation  
- **XGBoost** – Advanced boosting algorithm for improved accuracy  
- **Statsmodels** – Statistical modeling and hypothesis testing  

---

## 📂 Project Structure
```
Medical-Insurance-Prediction/
│── data/
│   ├── insurance.csv  # Dataset
│── notebooks/
│   ├── EDA.ipynb  # Exploratory Data Analysis
│   ├── Model_Training.ipynb  # Training and Evaluating Models
│── src/
│   ├── data_preprocessing.py  # Data cleaning and feature engineering
│   ├── train_model.py  # Training ML models
│── README.md  # Project documentation
│── requirements.txt  # Dependencies
│── app.py  # Flask API for predictions
│── model.pkl  # Trained model file
```

---

## 🚀 Installation & Setup
### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/Medical-Insurance-Prediction.git
cd Medical-Insurance-Prediction
```

### 2️⃣ Create a Virtual Environment
```bash
python -m venv venv
source venv/bin/activate  # MacOS/Linux
venv\Scripts\activate  # Windows
```

### 3️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 4️⃣ Run Jupyter Notebooks
To explore the dataset and model performance, run:
```bash
jupyter notebook
```

---

## 🤖 Machine Learning Models Used
The project explores multiple regression models for predicting insurance costs:

| Model | Train R² | Test R² | RMSE (Test) |
|--------|---------|---------|------------|
| **Linear Regression** | 0.75 | 0.74 | 6,193.94 |
| **Decision Tree** | 1.00 | 0.76 | 5,800.12 |
| **Random Forest** | 0.97 | 0.82 | 4,900.55 |
| **XGBoost** | 0.90 | 0.86 | 4,200.89 |

---

## 📊 Model Evaluation Metrics
The models were evaluated using:

- **R² Score** – Measures how well the model explains variance in insurance charges.  
- **Root Mean Squared Error (RMSE)** – Measures prediction error in dollars.  
- **Mean Absolute Error (MAE)** – Average absolute differences between actual and predicted values.  

---

## 🔥 How to Use the Prediction Model
### 1️⃣ Running the Flask API
To deploy the model as an API:
```bash
python app.py
```
This will start a local server for real-time predictions.

### 2️⃣ Making a Prediction
You can send a request using `curl` or Postman:
```bash
curl -X POST http://127.0.0.1:5000/predict \
-H "Content-Type: application/json" \
-d '{"age": 35, "sex": "male", "bmi": 28.5, "children": 2, "smoker": "no", "region": "northeast"}'
```
📌 The API will return the **predicted insurance cost** in JSON format.

---

## 🔮 Future Improvements
- ✅ Incorporate **deep learning models (ANNs)** for enhanced accuracy.
- ✅ Implement **SHAP (SHapley Additive exPlanations)** for better feature interpretability.
- ✅ Deploy as a **Streamlit web app** for an interactive UI.
- ✅ Extend the model to **larger datasets and different regions**.

---

## 🤝 Contributing
Contributions are welcome! Follow these steps:

1. **Fork the repository**  
2. **Create a new branch** (`git checkout -b feature-name`)  
3. **Make your changes and commit** (`git commit -m "Added new feature"`)  
4. **Push to your branch** (`git push origin feature-name`)  
5. **Create a pull request** 🚀  

---

## 🏆 Acknowledgments
This project is inspired by real-world applications in **health insurance and risk assessment**. Thanks to the **open-source community** for the amazing tools and libraries!

💡 **Let’s connect!** If you’re passionate about machine learning and predictive analytics, feel free to reach out.

📧 **Contact**: toshineb@gmail.com  
🌐 **LinkedIn**: (https://www.linkedin.com/in/tosinbellofin/)  

---

## 📜 License
This project is licensed under the **MIT License** – feel free to use and modify it for your own work.

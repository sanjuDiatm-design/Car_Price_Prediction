# 🚗 Car Price Prediction API

A **Machine Learning-powered Car Price Prediction application** built with **Python, Scikit-learn, FastAPI, and Streamlit**.

The project uses a **Random Forest Regression model** to predict the estimated selling price of a used car based on features such as year, present price, kilometers driven, fuel type, seller type, transmission, and other vehicle-related attributes.

---

## 🚀 Features

* 🤖 Machine Learning-based car price prediction
* 🌲 Random Forest Regression model
* ⚡ FastAPI REST API
* 🎨 Streamlit web interface
* ✅ Input validation using Pydantic
* 📊 Car price prediction from vehicle features
* 🔄 Pre-trained model stored using Joblib
* 📁 Feature column management for consistent model input
* 🐍 Python-based end-to-end ML application

---

## 🛠️ Technologies Used

| Technology   | Purpose              |
| ------------ | -------------------- |
| Python       | Programming language |
| Pandas       | Data processing      |
| NumPy        | Numerical operations |
| Scikit-learn | Machine Learning     |
| Joblib       | Model serialization  |
| FastAPI      | REST API             |
| Pydantic     | Data validation      |
| Uvicorn      | ASGI server          |
| Streamlit    | Web interface        |

---

## 📂 Project Structure

```text
Car_Price_Prediction/
│
├── main.py
├── model.py
├── schema.py
├── train.py
├── streamlit_app.py
│
├── cardekho_data.csv
├── random_forest_model.pkl
├── feature_columns.pkl
│
├── requirements.txt
├── runtime.txt
├── LICENSE
└── .gitignore
```

---

## 🧠 Machine Learning Model

The project uses a **Random Forest Regressor** for predicting car prices.

### Workflow

```text
Car Dataset
     ↓
Data Preprocessing
     ↓
Feature Engineering
     ↓
Train/Test Split
     ↓
Random Forest Regression
     ↓
Model Evaluation
     ↓
Save Trained Model
     ↓
FastAPI / Streamlit
     ↓
Car Price Prediction
```

The trained model is saved as:

```text
random_forest_model.pkl
```

The feature columns required by the model are saved as:

```text
feature_columns.pkl
```

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/sanjuDiatm-design/Car_Price_Prediction.git
```

Move into the project directory:

```bash
cd Car_Price_Prediction
```

---

### 2. Create a virtual environment

Windows:

```powershell
python -m venv myenv
```

Activate it:

```powershell
myenv\Scripts\activate
```

---

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

# ⚡ Run FastAPI

Start the FastAPI application using:

```bash
uvicorn main:app --reload
```

The API will run at:

```text
http://127.0.0.1:8000
```

---

## 📖 FastAPI Documentation

FastAPI automatically provides interactive API documentation.

### Swagger UI

```text
http://127.0.0.1:8000/docs
```

### ReDoc

```text
http://127.0.0.1:8000/redoc
```

You can use Swagger UI to enter car information and test the prediction API directly from your browser.

---

# 🎨 Run Streamlit

To start the Streamlit interface:

```bash
streamlit run streamlit_app.py
```

Streamlit will provide a local URL similar to:

```text
http://localhost:8501
```

---

## 🔌 API Usage

The API accepts vehicle information and returns the predicted car price.

Example request:

```json
{
    "year": 2018,
    "present_price": 5.59,
    "kms_driven": 27000,
    "fuel_type": "Petrol",
    "seller_type": "Dealer",
    "transmission": "Manual",
    "owner": 0
}
```

Example response:

```json
{
    "predicted_price": 4.85
}
```

> The exact prediction depends on the trained Random Forest model and input features.

---

## 📊 Dataset

The project uses a used-car dataset containing information about vehicles and their selling prices.

Important features include:

* Year
* Present Price
* Kilometers Driven
* Fuel Type
* Seller Type
* Transmission
* Owner
* Selling Price

The dataset is included in:

```text
cardekho_data.csv
```

---

## 🧪 Model Training

If you want to retrain the model, run:

```bash
python train.py
```

This process generates the trained model and feature information used by the API.

---

## 📌 API Architecture

```text
                User
                  │
                  ▼
          FastAPI / Streamlit
                  │
                  ▼
            Input Validation
               Pydantic
                  │
                  ▼
          Feature Preparation
                  │
                  ▼
        Random Forest Model
                  │
                  ▼
          Price Prediction
                  │
                  ▼
             API Response
```

---

## 🔒 Environment & Security

Sensitive files and local environments should not be committed to GitHub.

The project `.gitignore` excludes:

```text
myenv/
venv/
.env
__pycache__/
*.pyc
.vscode/
```

---

## 🔮 Future Improvements

* 🌐 Deploy FastAPI to a cloud platform
* 🚀 Deploy Streamlit application
* 📈 Add model performance metrics
* 📊 Add data visualization dashboard
* 🔐 Add API authentication
* 🗄️ Store predictions in a database
* 📱 Improve responsive UI
* 🧠 Experiment with XGBoost, Gradient Boosting, and other regression algorithms
* 📦 Add Docker support
* 🧪 Add automated tests

---

## 👨‍💻 Author

**Sanju Ghosh**

GitHub:
https://github.com/sanjuDiatm-design/Car_Price_Prediction

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub!

---

## 📄 License

This project is licensed under the **MIT License**.

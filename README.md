This repository contains two end-to-end data science and machine learning Tasks:

- **Task 1 – Titanic Survival Classification**
- **Task 2 – Stock Price Prediction using LSTM**

# 🚢 Task 1: Titanic Survival Classification

## 🎯 Objective
Predict whether a passenger survived the Titanic disaster using machine learning algorithms.

---

## 📊 Workflow

### **1. Importing Libraries**
- pandas  
- numpy  
- matplotlib  
- seaborn  
- sklearn  

### **2. Data Loading**
- Loaded **Titanic-Dataset.csv**
- Inspected shape, data info, and descriptive statistics.

### **3. Exploratory Data Analysis**
Performed visual and statistical exploration:
- Checked missing values  
- Plots:
  - Survival vs Gender  
  - Survival vs Passenger Class  
  - Age distribution  
  - Fare distribution  
  - Missing value heatmap  

### **4. Data Cleaning**
- Filled missing **Age** with median  
- Filled **Embarked** with mode  
- Dropped:
  - Cabin (high missing rate)
  - Ticket  
  - PassengerId  
  - Name  

### **5. Feature Engineering**
- Encoded **Sex** → (0 = male, 1 = female)  
- One-hot encoding for **Embarked**  
- Created:
  - `FamilySize = SibSp + Parch + 1`
  - `IsAlone` flag  
- Scaled numerical columns (**Age**, **Fare**)

### **6. Train/Test Split**
- Used **80/20 split**

### **7. Models Trained**
- Logistic Regression  
- Random Forest  
- K-Nearest Neighbors (KNN)

### **8. Model Evaluation**
Evaluated using:
- Accuracy  
- Confusion Matrix  
- Classification Report  
- Heatmaps  
- Model comparison bar chart  

### **🏆 Best Model**
- **Random Forest** → *83.24% accuracy*  
- **KNN** → *83.24% accuracy*  

---

# 📈 Task 2: Stock Price Prediction (LSTM)

## 🎯 Objective
Predict next-day **Adjusted Close** prices using deep learning (LSTM).

---

## 📊 Workflow

### **1. Libraries Used**
- pandas  
- numpy  
- matplotlib  
- seaborn  
- tensorflow.keras  
- MinMaxScaler  

### **2. Data Loading**
- Loaded **MB_dataset.csv** (OHLCV stock dataset)

### **3. Exploratory Data Analysis**
Performed:
- Shape, info, statistical summary  
- Plots:
  - Open & Close price trend  
  - Trading volume trend  

### **4. Data Preparation**
- Converted Date → datetime  
- Set Date as index  
- Dropped Close column  
- Feature Engineering:
  - Moving averages: **MA5**, **MA10**, **MA20**
  - Daily return  
  - Price range (High − Low)
  - Lag features: **Lag1**, **Lag5**

### **5. Scaling**
- Applied **MinMaxScaler** to features and target

### **6. Creating LSTM Sequences**
- Used **60-day sliding window**
- Created `X` and `y` for LSTM training

### **7. Train/Test Split**
- **80%** → Training  
- **20%** → Testing  

### **8. LSTM Model Architecture**
- LSTM(50, return_sequences=True)  
- Dropout(0.2)  
- LSTM(50)  
- Dropout(0.2)  
- Dense(1)  

### **9. Model Training**
- 50 epochs  
- Batch size: 32  
- Validation split: 10%  

### **10. Predictions**
- Generated scaled predictions  
- Applied inverse scaling  
- Visualized actual vs predicted prices  

### **11. Evaluation Metrics**

| Metric | Value |
|--------|--------|
| **MSE** | 3.4457 |
| **RMSE** | 1.8562 |
| **MAE** | 1.4419 |

---

# 🛠️ Technologies Used

## 📌 Machine Learning
- Logistic Regression  
- Random Forest  
- KNN  

## 📌 Deep Learning
- LSTM Neural Network  

## 📌 Tools & Libraries
- Python  
- Pandas / NumPy  
- Matplotlib / Seaborn  
- Scikit-learn  
- TensorFlow / Keras  

---

# 🎯 Learning Outcomes
- Data cleaning & preprocessing  
- Handling missing values  
- Feature engineering (ML + time-series)  
- Train/test splitting  
- ML model evaluation  
- LSTM sequence generation  
- Time-series forecasting  
- Result visualization  

---

# 👨‍💻 Author
**Muhammad Arhum**  
MS Computer Science | Data Science Enthusiast  

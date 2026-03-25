# 🏠 House Price Prediction using Machine Learning

Welcome to my first Machine Learning project! In this project, I built a **Multiple Linear Regression** model to predict house prices based on physical features of the property.

---

## 🚀 Project Overview
The goal of this project was to understand the relationship between a house's attributes (like area and number of rooms) and its market price. I moved from a **Simple Linear Regression** (1 feature) to a **Multiple Linear Regression** (5 features) to improve accuracy.

### 📊 The Dataset
I used the `Housing.csv` dataset. While the dataset contains many categorical features (like 'mainroad' or 'basement'), for this initial version, I focused strictly on the **numerical columns** to train the model.

**Features used for training:**
* 📐 `area`: Total square footage
* 🛏️ `bedrooms`: Number of bedrooms
* 🚿 `bathrooms`: Number of bathrooms
* 🧱 `stories`: Number of floors
* 🚗 `parking`: Number of parking spaces

---

## 📈 Initial Data Visualization
Before training, I plotted the raw data to see if there was a trend.

<img width="1140" height="909" alt="Screenshot 2026-03-25 222003" src="https://github.com/user-attachments/assets/ee57d7c4-7c93-4934-b426-fe9b77e26b06" />

> **Observation:** There is a clear positive correlation—as the area increases, the price generally goes up!

---

## 🛠️ The Machine Learning Pipeline
I followed a standard 7-step process to build this model:

1. **Define Variables:** Isolated my features (**X**) and the target price (**y**).
2. **Data Splitting:** Divided the data into **80% Training** (to teach the model) and **20% Testing** (to evaluate it).
3. **Exploratory Visualization:** Plotted Area vs. Price.
4. **Model Training:** Initialized the `LinearRegression` model and used the `.fit()` function.
5. **Prediction:** Generated price guesses for the test dataset.
6. **Evaluation:** Measured accuracy using **MAE** and **R² Score**.
7. **Final Visualization:** Plotted the "Line of Perfection."

---

## 🧪 Model Results
By using multiple features, I significantly improved the model's performance:

* **Mean Absolute Error (MAE):** ~1.02M
* **R² Score:** **0.6004** (The model explains about 60% of the price variation!)

### Actual vs. Predicted Prices
This graph shows how close the model's guesses (blue dots) are to the actual truth (red line).

<img width="1698" height="1094" alt="image" src="https://github.com/user-attachments/assets/659727ef-bc29-496e-a3a6-50d78498758c" />

---

## 🛠️ Tech Stack
* **Language:** Python 🐍
* **Libraries:** Pandas, NumPy, Matplotlib, Scikit-Learn
* **Environment:** Google Colab / Jupyter Notebook

---

## 🔜 What's Next?
Currently, the model ignores columns like `mainroad` and `airconditioning` because they are text ("yes"/"no"). We can do **Label Encoding** to turn these into numbers and push that R² score even higher! 🚀

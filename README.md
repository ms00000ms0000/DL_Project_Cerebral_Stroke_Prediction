# 🧠 Cerebral Stroke Prediction System — Deep Learning Model

## 📘 Project Description

The **Cerebral Stroke Prediction System** is a Deep Learning-based project that predicts whether a person is at risk of a **stroke** using medical, demographic, and lifestyle features.
Built with a **Sequential Artificial Neural Network (ANN)**, this model achieves around **98% accuracy**, making it highly effective for early stroke risk assessment.

---

## 🔍 About the Project

This project demonstrates how deep learning can be applied to healthcare data to predict stroke risk.
It uses patient medical and lifestyle data and applies data preprocessing, missing-value handling, encoding, standardization, model training, and evaluation to classify stroke risk accurately.

---

## 🧠 Model Architecture

The model is a **Sequential Neural Network** built using **TensorFlow/Keras**, consisting of:

* **Input Layer:** Features — `gender`, `age`, `hypertension`, `heart_disease`, `ever_married`, `work_type`, `Residence_type`, `avg_glucose_level`, `bmi`, `smoking_status`
* **Hidden Layers:** Fully connected `Dense` layers using **ReLU** activation
* **Output Layer:** Uses **Sigmoid** activation for binary classification
* **Optimizer:** **Adam**
* **Loss Function:** **Binary Cross-Entropy**
* **Metric:** **Accuracy**

The model uses a threshold on the sigmoid output to determine the final binary class (0 = No Stroke, 1 = Stroke).

---

## 🧾 Dataset Description

The dataset contains patient medical and lifestyle information used for stroke prediction.

| Column              | Description                                           |
| :------------------ | :---------------------------------------------------- |
| `gender`            | Gender of the person                                  |
| `age`               | Age in years                                          |
| `hypertension`      | 0 — No, 1 — Yes                                       |
| `heart_disease`     | 0 — No, 1 — Yes                                       |
| `ever_married`      | Whether the person is married                         |
| `work_type`         | Type of employment                                    |
| `Residence_type`    | Urban or Rural                                        |
| `avg_glucose_level` | Average blood glucose level                           |
| `bmi`               | Body Mass Index (null values replaced with **mean**)  |
| `smoking_status`    | Smoking category (null values replaced with **mode**) |
| `stroke`            | Target variable — 0(No) / 1(Yes)                      |

The target variable **`stroke`** is used for binary classification after preprocessing.

---

## ⚙️ Tech Stack & Libraries

**Languages:**

* Python 🐍

**Libraries & Frameworks:**

* **TensorFlow / Keras** – Deep Learning Model
* **NumPy** – Numerical Computations
* **Pandas** – Data Handling
* **Matplotlib** – Visualization
* **Scikit-learn (sklearn)** – Preprocessing, Label Encoding, Scaling, and Data Splitting

---

## 🚀 Features

* Predicts stroke risk using deep learning
* Handles missing values using mean (for `bmi`) and mode (for `smoking_status`)
* Standardizes features using **StandardScaler**
* Trained using **Adam** optimizer and **binary_crossentropy** loss
* Achieves **~98% accuracy** on test data
* Easily retrainable with updated medical datasets

---

## 📊 Results

The trained ANN model achieved **~98% accuracy**, effectively classifying individuals as **Stroke** or **No Stroke** based on health indicators.
Model performance was validated using held-out test data and sample predictions.

---

## 📁 Repository Structure

```
📦 DL_Project_Cerebral_Stroke_Prediction
│
├── IBM_DL_Model_Cerebral_Stroke.ipynb                                    # Jupyter Notebook with full project code
├── dataset.csv                                                           # Dataset used for training (if included)
└── README.md                                                             # Project documentation (this file)
```

---

## 🧪 How to Run

1. ## Clone the repository:

   ```bash
   git clone https://github.com/<your-username>/DL_Project_Cerebral_Stroke_Prediction.git
   cd DL_Project_Cerebral_Stroke_Prediction
   ```

2. ## Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. ## Run the notebook:

   ```bash
   jupyter notebook IBM_DL_Model_Cerebral_Stroke.ipynb
   ```

4. ## Train and test the model — predictions and sample inferences will be shown at the end of the notebook.

---

## 📈 Future Improvements

* Integrate real-time hospital / wearable health data for continuous monitoring
* Deploy using **Flask** or **Streamlit** for clinical usage
* Add explainability using **SHAP** or **LIME** to interpret model decisions
* Experiment with time-series or ensemble models (LSTM, CNN, or ensembles) for robustness
* Create a mobile-friendly frontend for health workers in rural areas

# Diabetes Prediction with ANN & Hyperparameter Tuning

This project implements a **Sequential Artificial Neural Network (ANN)** to predict diabetes using the **PIMA Indians Diabetes Dataset**.  
The focus of this project is **learning how to perform hyperparameter tuning** using **Keras Tuner (Random Search) And GridSearch**.  

⚠ **Note:**  
This is a *learning project* for understanding hyperparameter tuning concepts.  
There is **no comparison of "before tuning" vs "after tuning" accuracy** because the untuned model had only 2 layers, while the tuned model has a variable number of layers (and other parameters). In fact, the untuned model might have shown *higher* accuracy simply because it had a simpler architecture and was not constrained by the tuning parameters — the aim here is learning the process, not beating a baseline.

---

## 📌 Features
- Load and preprocess dataset using `pandas` and `StandardScaler`
- Build a binary classification ANN using TensorFlow/Keras
- Tune hyperparameters such as:
  - Number of layers
  - Units per layer
  - Dropout rates
  - Learning rate
- Use **Random Search** strategy from Keras Tuner
- Evaluate the tuned model on test data

---

## 🛠 Tech Stack
- **Python**
- **Pandas** & **NumPy**
- **Scikit-learn**
- **TensorFlow/Keras**
- **Keras Tuner**

---

## 📂 Dataset
We use the **PIMA Indians Diabetes Dataset**, which contains health parameters like glucose levels, BMI, age, and more.  
You can download it from [Kaggle](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database) or use the CSV provided in the project.

---

## 🚀 How to Run

1. **Clone the repository**
```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```
2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Run the notebook**

- Open diabetes_ann.ipynb in Google Colab or Jupyter Notebook
- Run cells step-by-step to see the preprocessing, model creation, and tuning

# 📊 Hyperparameter Tuning with keras-tuner Details

- We use Keras Tuner to explore:
- Units in each layer (8–128)
- Number of layers (2–5)
- Dropout rate (0.0–0.5)
- Learning rate (1e-4 to 1e-1)

# 📊 Hyperparameter Tuning with GridSearch Details
- Layers List : [16,32], [16, 32, 16], [16, 8, 16, 32]
- Activation ['sigmoid','relu']
- batch_size [125,256]

# 🧠 Learning Outcomes

- Understanding how to structure a deep learning project
- Implementing binary classification with ANN
- Applying hyperparameter tuning with Keras Tuner
- Realizing that accuracy differences are not always the main focus when learning tuning techniques

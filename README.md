# 📧 Spam Mail Detection using Machine Learning and NLP

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:4F46E5,100:7C3AED&height=220&section=header&text=Spam%20Mail%20Detection&fontSize=40&fontColor=ffffff&animation=fadeIn&fontAlignY=40" />
</p>

<div align="center">

![Python](https://img.shields.io/badge/Python-3.13-blue?style=for-the-badge\&logo=python)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-blue?style=for-the-badge\&logo=numpy)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-black?style=for-the-badge\&logo=pandas)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange?style=for-the-badge\&logo=scikitlearn)
![NLP](https://img.shields.io/badge/NLP-Text%20Processing-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

</div>

---

# 📌 Project Overview

This project focuses on building a **Spam Mail Detection System** using **Machine Learning** and **Natural Language Processing (NLP)** techniques.

The model analyzes email content and classifies messages as:

* 📩 Ham (Legitimate Email)
* 🚫 Spam (Unwanted Email)

To achieve this, email text is converted into numerical features using **TF-IDF Vectorization**, and a **Logistic Regression** model is trained to perform binary classification.

---

# 🎯 Problem Statement

Email spam remains one of the most common challenges in digital communication. Manually filtering spam emails is inefficient and time-consuming.

The objective of this project is to develop a machine learning model capable of automatically identifying and classifying emails as Spam or Ham based on their textual content.

---

# 📂 Dataset Information

The dataset contains email messages and their corresponding labels.

### Features

| Feature | Description   |
| ------- | ------------- |
| Message | Email Content |

### Target Variable

| Target   | Description |
| -------- | ----------- |
| Category | Spam or Ham |

### Label Encoding

| Category | Encoded Value |
| -------- | ------------- |
| Ham      | 1             |
| Spam     | 0             |

---

# 🛠️ Technologies Used

| Technology          | Purpose                 |
| ------------------- | ----------------------- |
| Python              | Programming Language    |
| NumPy               | Numerical Computing     |
| Pandas              | Data Manipulation       |
| Scikit-Learn        | Machine Learning        |
| TF-IDF Vectorizer   | Feature Extraction      |
| Logistic Regression | Classification Model    |
| Jupyter Notebook    | Development Environment |

---

# 🔄 Machine Learning Workflow

```text
1. Data Collection
2. Data Exploration
3. Data Preprocessing
4. Label Encoding
5. Train-Test Split
6. TF-IDF Feature Extraction
7. Model Training
8. Model Evaluation
9. Spam Mail Prediction
```

---

# 📊 Exploratory Data Analysis

The dataset was explored to:

* Understand dataset structure
* Check missing values
* Analyze class distribution
* Identify unique categories

Key Operations:

```python
df.info()
df.isnull().sum()
df['Category'].value_counts()
pd.unique(df['Category'])
```

---

# 🛠️ Data Preprocessing

Data preprocessing included:

* Label Encoding
* Separating Features and Labels
* Splitting Training and Testing Data
* Text Cleaning through TF-IDF Vectorization

### Feature Variable

```python
X = df['Message']
```

### Target Variable

```python
Y = df['Category']
```

---

# 🔤 TF-IDF Feature Extraction

Machine learning models cannot directly understand textual data.

Therefore, **TF-IDF (Term Frequency-Inverse Document Frequency)** is used to transform text into numerical vectors.

### Benefits

* Converts text into machine-readable format
* Reduces importance of common words
* Highlights meaningful keywords
* Improves classification performance

```python
feature_extraction = TfidfVectorizer(
    min_df=1,
    stop_words='english',
    lowercase=True
)
```

---

# 🤖 Model Selection

## Logistic Regression

Logistic Regression is a supervised machine learning algorithm used for binary classification problems.

### Why Logistic Regression?

* Simple and effective
* Fast training
* High interpretability
* Strong performance on text classification tasks

```python
model = LogisticRegression()
```

---

# 🏋️ Model Training

The Logistic Regression model was trained using the TF-IDF transformed training dataset.

```python
model.fit(X_train_num, Y_train)
```

The model learns patterns and relationships between email content and their corresponding labels.

---

# 📈 Model Evaluation

The trained model was evaluated on both training and testing datasets.

### Training Accuracy

```python
training_data_accuracy = accuracy_score(
    X_train_prediction,
    Y_train
)
```

### Testing Accuracy

```python
test_data_accuracy = accuracy_score(
    X_test_prediction,
    Y_test
)
```

The model achieved high accuracy in distinguishing spam emails from legitimate emails.

---

# 📧 Spam Mail Prediction System

The trained model can classify new email messages.

### Example Input

```python
input_data = [
    "Congratulations! You've won a free ticket to the Bahamas! Click here to claim now."
]
```

### Example Output

```text
Spam Mail
```

---

# 📁 Project Structure

```text
Spam-Mail-Detection/
│
├── mail_data.csv
├── Spam_Mail_Detection.ipynb
├── README.md
├── requirements.txt
└── screenshots/
```

---

# ▶️ How to Run the Project

### Clone the Repository

```bash
git clone https://github.com/your-username/Spam-Mail-Detection.git
```

### Navigate to Project Directory

```bash
cd Spam-Mail-Detection
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Spam_Mail_Detection.ipynb
```

---

# 🚀 Future Improvements

* Deploy as a web application
* Build a real-time spam filtering system
* Experiment with Naive Bayes and SVM models
* Use larger datasets
* Explore Deep Learning approaches
* Integrate with email clients

---

# 📚 Skills Demonstrated

✅ Python Programming

✅ Data Analysis with Pandas

✅ Data Preprocessing

✅ Natural Language Processing (NLP)

✅ TF-IDF Vectorization

✅ Machine Learning Classification

✅ Logistic Regression

✅ Model Evaluation

✅ Predictive Systems

---

# 👨‍💻 Author

**Mehar**

Aspiring AI Engineer | Machine Learning Enthusiast | Data Science Learner

🚀 Continuing my journey in Generative AI, Machine Learning, Data Science, and Python through hands-on projects and continuous learning.

---

<div align="center">

### ⭐ If you found this project useful, consider giving it a star!

</div>


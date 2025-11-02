# 🧠 Sentiment Analysis on Swiggy Reviews using RNN

## 📘 Project Overview

This project focuses on performing **Sentiment Analysis** on **Swiggy customer reviews** using a **Recurrent Neural Network (RNN)** built with **TensorFlow and Keras**.
The goal is to automatically classify customer feedback as **positive** or **negative**, helping to understand user satisfaction and improve restaurant services.

By analyzing textual reviews and ratings, this project demonstrates how **deep learning** techniques can extract valuable insights from real-world customer data.

---

## 📊 Dataset Description

The dataset used in this project (`swiggy.csv`) contains various details about restaurants and customer feedback.
Key columns include:

| Column Name        | Description                      |
| ------------------ | -------------------------------- |
| `ID`               | Unique identifier for each entry |
| `Area`             | Area or region of the restaurant |
| `City`             | City name                        |
| `Restaurant Price` | Average price level              |
| `Avg Rating`       | Average customer rating          |
| `Total Rating`     | Number of ratings received       |
| `Food Item`        | Name of the food item            |
| `Food Type`        | Vegetarian/Non-Vegetarian        |
| `Delivery Time`    | Delivery time in minutes         |
| `Review`           | Textual customer review          |

The **target variable** (`sentiment`) was created based on the **Avg Rating**:

* Rating > 3.5 → **Positive Sentiment (1)**
* Rating ≤ 3.5 → **Negative Sentiment (0)**

---

## 🧹 Data Preprocessing

The text data underwent several preprocessing steps before training:

1. Converted all reviews to lowercase
2. Removed punctuation, numbers, and special characters
3. Tokenized the text and padded sequences to equal length
4. Split the dataset into training, validation, and testing sets

---

## 🧩 Model Architecture

A **Simple RNN** model was implemented using TensorFlow/Keras with the following layers:

```
Embedding(input_dim=5000, output_dim=16, input_length=200)
SimpleRNN(64, activation='tanh')
Dense(1, activation='sigmoid')
```

**Loss Function:** Binary Crossentropy
**Optimizer:** Adam
**Metrics:** Accuracy

---

## ⚙️ Training Details

* **Epochs:** 5
* **Batch Size:** 32
* **Training Accuracy:** ~72%
* **Validation Accuracy:** ~71.5%
* **Test Accuracy:** **72%**

---

## 🧪 Model Evaluation and Results

After training, the model achieved a **Test Accuracy of 72%**, showing it effectively classifies customer sentiment.

Example prediction:

```python
Review: "The food was great."
Sentiment: Positive (Probability: 0.71)
```

This demonstrates that the model successfully identifies sentiment from unseen reviews.


## 🧰 Technologies Used

* **Python 3**
* **TensorFlow / Keras**
* **Pandas & NumPy**
* **Scikit-learn**
* **Matplotlib**
* **Regular Expressions (re)**


# SMS Spam Classifier (NLP)

### Project Overview
This project involves building a **Natural Language Processing (NLP)** model to classify SMS messages as either **"ham"** (normal messages) or **"spam"** (advertisements/automated messages). Using the SMS Spam Collection dataset, I developed a machine learning pipeline to process raw text and predict the probability of a message being spam.

### Machine Learning Highlights
*   **Text Pre-processing:** Implemented tokenization and text normalization to convert raw strings into numerical tensors suitable for machine learning.
*   **Binary Classification:** Developed a model that outputs both a probability score ($0.0$ to $1.0$) and a categorical label ("ham" vs. "spam").
*   **End-to-End Pipeline:** Created a robust `predict_message` function designed for real-time inference on unseen text strings.

---

### Technical Methodology

#### **1. Data Preparation**
*   **Dataset:** Utilized the SMS Spam Collection dataset, already partitioned into training and testing sets.
*   **Label Encoding:** Mapped categorical labels ("ham", "spam") to numerical values for model training.

#### **2. NLP Workflow**
*   **Vectorization:** Transformed text data into a numerical format (using techniques such as **TF-IDF** or **Word Embeddings**) to capture the semantic meaning of the messages.
*   **Model Selection:** Trained a classification model (such as an **LSTM, RNN, or Naive Bayes**) to identify patterns frequently found in spam messages (e.g., "WINNER", "FREE", "URGENT").

#### **3. Inference Function**
*   Designed the `predict_message` function to return a structured list:
    *   **Index 0:** A float representing the "spamminess" (0 for pure ham, 1 for certain spam).
    *   **Index 1:** The predicted string label based on a $0.5$ probability threshold.

---

### View the Analysis: **[View the SMS Spam Classifier Notebook](./sms_spam_classifier.ipynb)**

### Tech Stack
*   **Frameworks:** TensorFlow / Keras (or Scikit-Learn)
*   **NLP Techniques:** Tokenization, Padding, Text Vectorization
*   **Libraries:** Pandas, NumPy, Matplotlib
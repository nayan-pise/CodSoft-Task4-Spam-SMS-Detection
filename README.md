# CodSoft-Task4-Spam-SMS-Detection
An NLP-based classifier to identify SMS messages as 'Spam' or 'Ham' (Legitimate). Implemented TF-IDF Vectorization to convert text data into numbers and used the Multinomial Naive Bayes algorithm for accurate prediction. Achieved high accuracy on the test set.
## 📂 Dataset
The dataset used for this project is the **SMS Spam Collection Dataset**, available on Kaggle. It contains a set of SMS messages in English that have been classified as either "Ham" (Legitimate) or "Spam".

* **Download Link:** [Kaggle - SMS Spam Collection Dataset](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset)
* **File Name:** `spam.csv`
* **Encoding Note:** The dataset requires `encoding='latin-1'` when loading with Pandas due to special characters in the text.

## ⚙️ Methodology & Workflow

The project follows a standard Machine Learning pipeline for Natural Language Processing (NLP):

1.  **Data Loading & Cleaning:**
    * Loaded the dataset using Pandas with `latin-1` encoding.
    * Removed unnecessary columns (`Unnamed: 2`, `Unnamed: 3`, `Unnamed: 4`).
    * Renamed columns to `Category` and `Message` for clarity.
    * Converted labels to numerical format: **Spam = 1**, **Ham = 0**.

2.  **Exploratory Data Analysis (EDA):**
    * Visualized the distribution of Spam vs. Ham messages to understand class balance.

3.  **Text Preprocessing (Feature Extraction):**
    * Split the data into Training (80%) and Testing (20%) sets.
    * Used **TF-IDF Vectorizer** (Term Frequency-Inverse Document Frequency) to convert raw text messages into numerical feature vectors that the machine learning model can understand.

4.  **Model Training:**
    * Implemented the **Multinomial Naive Bayes** algorithm. This algorithm is highly effective for text classification tasks because it handles discrete frequency counts (like word counts) very well.

5.  **Model Evaluation:**
    * Evaluated the model using **Accuracy Score**, **Confusion Matrix**, and **Classification Report**.
    * Achieved high accuracy on the unseen test data.

6.  **Prediction System:**
    * Built a function that takes new user input (a text message), processes it, and predicts whether it is Spam or Ham.

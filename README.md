# Spam SMS Detection

## Objective

The objective of this project is to classify SMS messages as spam or not spam based on the content of the message. By detecting spam messages, the system can help filter unwanted communication and improve user experience in messaging applications.

---

## Dataset

The dataset used in this project is available on Kaggle:  
[Kaggle Dataset Link](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset)

---

## Steps Taken

### 1. Data Preprocessing
- **Text Preprocessing:** Applied several NLP techniques to clean and prepare the data:
  - **Stopwords Removal:** Removed common words that do not add significant meaning.
  - **Tokenization:** Split messages into individual words (tokens).
  - **Lemmatization:** Reduced words to their base or root form to standardize the text.

### 2. Feature Extraction
- **TF-IDF (Term Frequency-Inverse Document Frequency):** Converted text into numerical vectors based on the importance of terms in the document relative to the corpus.
- **Word2Vec:** Used Word2Vec embeddings to represent words as dense vectors, capturing semantic meaning from the text.

### 3. Model Building
- **Logistic Regression:** Trained a Logistic Regression model to classify SMS messages as spam or not spam.
- **Naive Bayes:** Trained a Naive Bayes model, which is known for its effectiveness in text classification tasks.
- **SVC (Support Vector Classifier):** Trained an SVC model to classify messages. However, the SVC model overfitted the data, especially when the kernel and hyperparameters were tuned.

### 4. Model Evaluation
- **Comparison:** After training the three models, it was found that:
  - **Logistic Regression** and **Naive Bayes** performed equally well with similar accuracy.
  - **SVC** showed signs of overfitting, performing well on the training set but not generalizing well to unseen data.
- **Final Model:** Chose **Logistic Regression** as the final model due to its balanced performance and simplicity.

---

## Kaggle Notebook

You can view the complete code implementation and analysis in my Kaggle notebook:  
[Kaggle Notebook Link](https://www.kaggle.com/code/varshithpsingh/spam-sms-detection)

---

## Insights and Results

- **Logistic Regression** and **Naive Bayes** both performed well, with similar accuracy rates for spam SMS detection.
- **SVC** overfitted the data, meaning it performed well on the training set but did not generalize well to the test set.
- **TF-IDF** embeddings proved to be more useful than **Word2Vec** for this specific task, contributing to better model performance.

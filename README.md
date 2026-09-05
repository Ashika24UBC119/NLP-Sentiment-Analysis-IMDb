# 🎬 NLP-Based Sentiment Analysis of IMDb Movie Reviews

## 📌 Project Overview

This project implements a Natural Language Processing (NLP) based Sentiment Analysis system for movie reviews.

The system analyzes a movie review and predicts whether the sentiment expressed in the review is **Positive** or **Negative**.

The project uses:

- Text Preprocessing
- TF-IDF (Term Frequency–Inverse Document Frequency)
- Logistic Regression
- Scikit-learn
- Gradio for the interactive application

## 🎯 Problem Statement

Movie reviews contain valuable opinions and emotions expressed through natural language. Manually analyzing thousands of reviews to determine whether they are positive or negative is time-consuming.

The objective of this project is to develop an NLP-based machine learning system that can automatically classify IMDb movie reviews into **Positive** or **Negative** sentiment categories.

## 🎯 Objectives

- To understand the application of NLP in sentiment analysis.
- To preprocess and clean movie review text.
- To convert textual data into numerical features using TF-IDF.
- To train a Logistic Regression classification model.
- To evaluate the model using Accuracy, Precision, Recall, F1-Score, and Confusion Matrix.
- To develop an interactive sentiment prediction application using Gradio.
  
## 📊 Dataset

### IMDb Large Movie Review Dataset

The dataset contains **50,000 movie reviews** divided into two sentiment classes:

| Sentiment | Number of Reviews |
|-----------|-------------------:|
| Positive  | 25,000 |
| Negative  | 25,000 |
| **Total** | **50,000** |

### Dataset Attributes

| Attribute | Description |
|----------|-------------|
| `review` | Text of the movie review |
| `sentiment` | Positive or Negative sentiment |

The sentiment labels were converted into numerical values:

- Positive → `1`
- Negative → `0`

### Train-Test Split

The dataset was divided using an **80:20 split**:

- Training data: 40,000 reviews
- Testing data: 10,000 reviews

## 🔄 Methodology

The project follows the workflow:

Movie Reviews
      ↓
Text Preprocessing
      ↓
TF-IDF Feature Extraction
      ↓
Logistic Regression
      ↓
Sentiment Prediction
      ↓
Model Evaluation
      ↓
Interactive Gradio Application

1. Text Preprocessing

The movie reviews were cleaned before training the model.

The preprocessing steps include:

Converting text to lowercase
Removing HTML tags
Removing special characters and numbers
Removing extra spaces

2. TF-IDF Feature Extraction

TF-IDF was used to convert the cleaned text into numerical feature vectors.

The project uses:

Maximum Features = 5000
Stop Words = English

TF-IDF helps identify words that are important for distinguishing between positive and negative reviews.

3. Logistic Regression

Logistic Regression was used as the classification algorithm.

The model was trained using the TF-IDF feature vectors and corresponding sentiment labels.

💻 Technologies Used
Programming Language
Python
Libraries
Pandas
NumPy
Matplotlib
Seaborn
Regular Expressions (re)
Scikit-learn
Gradio
Development Environment
Google Colab
GitHub

⚙️ Machine Learning Model

The classification model used in this project is:

Logistic Regression

Model configuration:

LogisticRegression(max_iter=1000)

The model predicts the sentiment of a review as either:

Positive

or

Negative

The prediction probability is also used to display the confidence of the prediction.

Results

The trained model achieved the following performance on the test dataset:

Metric	Score
Accuracy	88.66%
Precision	87.86%
Recall	89.72%
F1-Score	88.78%

The model was also evaluated using a Confusion Matrix and Classification Report.

🖥️ Interactive Application

The trained sentiment analysis model was integrated with Gradio to create an interactive web interface.

Users can enter a movie review and the application displays:

Predicted sentiment
Prediction confidence
Example
Input:
This movie was absolutely fantastic. The acting was brilliant!

Output:
Sentiment: Positive

Another example:

Input:
The movie was boring and disappointing. I hated it.

Output:
Sentiment: Negative

Screenshots of the application and model results are available in the screenshots/ folder.


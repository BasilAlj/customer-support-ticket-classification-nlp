Project Overview

This project explores multiclass customer support ticket classification using Natural Language Processing (NLP) and classical machine learning. The goal was to classify support tickets into five categories:

Billing inquiry
Cancellation request
Product inquiry
Refund request
Technical issue

The project used ticket text fields such as Ticket Subject and Ticket Description to train and evaluate classification models.

Objective

The main objective was to build a machine learning pipeline that could automatically route customer support tickets into the correct category based on their text content.

Methods

The following steps were performed during the project:

Text preprocessing and cleaning
TF-IDF vectorization
Baseline and comparison modeling using:
Multinomial Naive Bayes
Logistic Regression
Linear SVM
Feature engineering with:
combined subject + description text
stronger noise-word removal
n-grams
model tuning with different TF-IDF and SVM settings
Results

Several experiments were conducted to improve classification performance. The best result was achieved using:

cleaned combined text
TF-IDF with 1-gram to 3-gram
Linear SVM

Best Accuracy: 0.2267

Although the model improved slightly after stronger cleaning and tuning, the overall performance remained weak.

Key Finding

The most important result of this project was that the main limitation was not only the model, but the dataset itself.

During the investigation, the data showed several problems:

repetitive template language
noisy and generic text
weak alignment between ticket text and ticket type
overlapping vocabulary across classes
inconsistent patterns that reduced learnability

Because of this, the dataset did not provide a strong and stable signal for reliable multiclass classification.

Lesson Learned

This project reinforced an important machine learning principle:

Good models still depend on good data.

Even with reasonable preprocessing, feature engineering, and model tuning, performance will remain limited if the dataset is noisy, poorly structured, or weakly aligned with the target.

In other words:

Garbage in, garbage out.

Why This Project Was Still Valuable

Even though the final accuracy remained limited, this project provided strong practical experience in:

NLP preprocessing
feature engineering
model comparison
hyperparameter tuning
confusion matrix analysis
dataset diagnosis
understanding when weak performance is caused by data quality rather than only model choice
Tools Used
Python
pandas
scikit-learn
TF-IDF Vectorizer
Multinomial Naive Bayes
Logistic Regression
Linear SVM
matplotlib
Final Takeaway

This project became more than a text classification task. It became a case study in data quality, showing that machine learning success depends not only on algorithms, but also on whether the data contains a clear, consistent, and learnable pattern.

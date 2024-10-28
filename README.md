# Toxicity Detection in Social Media

This project aims to build a machine learning model that not only detects toxic behavior in social media comments but also rephrases harmful content into neutral or constructive language. The model is designed to identify various forms of toxicity such as hate speech, insults, and cyberbullying, while providing suggestions to foster better communication.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Evaluation](#evaluation)


## Introduction

Toxic content on social media platforms is a growing concern, leading to harmful consequences such as harassment, bullying, and misinformation. This project leverages state-of-the-art transformer models like **BERT** to detect toxic comments and uses **GPT-4o-mini** to rephrase toxic text. We aim to mitigate the negative impacts of online toxicity by suggesting constructive rephrasings that retain the original intent while reducing harmful language.

## Features

- **Toxic Comment Detection**: Identifies various forms of toxicity in text, including hate speech, insults, and threats.
- **Text Rephrasing**: Uses GPT-4o-mini to rephrase toxic comments into neutral or courteous forms.
- **Interpretability**: Provides insights into model decisions using SHAP (SHapley Additive exPlanations).
- **Custom Prompt-based Fine-tuning**: Fine-tuned BERT model for better performance on social media datasets.
- **Human-in-the-loop Evaluation**: Enables human moderators to assess the fluency, message retention, and reduction in toxicity of rephrased content.

## Dataset

The project uses the **Jigsaw Toxic Comment Classification** dataset, available on [Kaggle](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge). The dataset includes user comments labeled with varying levels of toxicity, categorized into the following classes:
- Toxic
- Severe Toxic
- Obscene
- Threat
- Insult
- Identity Hate

We have divided the dataset into 70% for training, 15% for validation, and 15% for testing.

## Model Architecture

### 1. **BERT for Toxicity Detection**
The core of the toxicity detection model is based on **BERT (Bidirectional Encoder Representations from Transformers)**, which captures subtle nuances in toxic language by processing the text bidirectionally. We fine-tuned the BERT model specifically for our task using the Jigsaw dataset.

### 2. **GPT-4o-mini for Text Rephrasing**
After detecting toxic comments, the model rephrases them using **GPT-4o-mini**, an advanced text-generation model. It is prompted to retain the original message while reducing toxicity.

### 3. **SHAP for Interpretability**
To ensure transparency in the model's decisions, we use **SHAP** values to explain why certain words or phrases were flagged as toxic. This makes the model’s predictions more interpretable for moderators and users.

## Evaluation
The model's effectiveness in detecting and rephrasing toxic content is assessed using several standard metrics:

1. **Accuracy**: Measures the overall percentage of correct predictions for both toxic and non-toxic comments.
2. **Precision**: Indicates the model's ability to correctly identify toxic comments out of all the comments it labeled as toxic.
3. **Recall**: Reflects the model's sensitivity in detecting all instances of toxic comments within the dataset.
4. **F1 Score**: Combines precision and recall to provide a balanced score that evaluates the model's ability to detect toxicity accurately and reliably.
5. **Support**: Refers to the number of actual occurrences of each label (toxic, non-toxic, etc.) in the dataset, providing context to the precision, recall, and F1 scores.


### Breakdown of Key Sections:
1. **Introduction**: Explains the goal of the project and its primary features (detection and rephrasing).
2. **Features**: Highlights the unique aspects of the project, such as interpretability and rephrasing.
3. **Dataset**: Information about the dataset used for training and testing.
4. **Model Architecture**: Provides details on the architecture, including BERT, GPT-4o-mini, and SHAP for interpretability.
6. **Evaluation**: Lists the metrics used to evaluate the performance of the model.

These metrics help us ensure that the model not only detects toxicity accurately but also effectively rephrases toxic language in a way that aligns with human evaluation. The metrics are computed on both the validation and test sets to provide a comprehensive assessment of model performance.

This `README.md` file gives a comprehensive overview of the project and provides all necessary instructions for users to run the model, evaluate it, and contribute to the repository.


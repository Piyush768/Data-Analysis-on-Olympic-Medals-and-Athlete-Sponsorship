# Olympics Analysis and Athlete Sponsorship Prediction

This project uses historical Olympics data to analyze patterns in athlete performance, predict potential medal winners, and recommend athletes for sponsorship based on Kellogg's criteria. The goal is to provide insights into athlete demographics, performance metrics, and sponsorship potential to aid in informed decision-making.

## Table of Contents
- [Overview](#overview)
- [Data](#data)
- [Analysis Process](#analysis-process)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Results](#results)
- [Recommendations](#recommendations)
- [Installation](#installation)
- [Usage](#usage)
- [Future Work](#future-work)

## Overview
Kellogg's aims to sponsor Olympic athletes based on historical performance, demographic insights, and medal prediction models. By leveraging athlete data, this project provides detailed analyses to support effective sponsorship decisions, focusing on identifying patterns among high-performing athletes across different Olympic events.

## Data
The dataset includes historical Olympic records detailing athlete performance, demographics, and medal achievements. Key features include:
- Athlete attributes: Name, nationality, age, height, weight
- Performance data: Event, year, medals won (Gold, Silver, Bronze)
- Event information: Sports category, season (Summer/Winter)

## Analysis Process
The project follows the CRISP-DM framework:

### 1. **Business Understanding**
   - Goal: Help Kellogg's select high-potential athletes for sponsorship by predicting likely medalists.
   - Key questions addressed:
     - What demographic features correlate with success?
     - How do performance trends differ across sports and seasons?

### 2. **Data Understanding**
   - Data overview, feature exploration, and missing value handling.
   - Visualization of key patterns, including age distribution, country dominance, and performance trends by event.

### 3. **Data Preparation**
   - Data cleaning and preprocessing (handling missing values, data transformations).
   - Creation of additional features relevant to sponsorship and performance metrics.

### 4. **Modeling**
   - Machine learning models applied to predict medal likelihood:
     - **Logistic Regression**
     - **Random Forest**
     - **Support Vector Classifier (SVC)**
     - **XGBoost**

## Evaluation
The models were evaluated based on key metrics:
- **AUPRC (Area Under Precision-Recall Curve)**: Evaluates how well the model balances precision and recall across thresholds, especially useful for identifying potential churners.
- **F1 Score**: Combines precision and recall to assess the model’s effectiveness in capturing true positive predictions.
- **Precision**: Measures the accuracy of positive predictions (correctly identified potential medalists).
- **Recall**: Measures the model’s ability to capture all relevant instances (identifying all medalists).

### Model Evaluation Summary:
- **Logistic Regression**:
  - **AUPRC**: 0.932
  - **F1**: 0.852
  - **Precision**: 0.848
  - **Recall**: 0.856
- **Random Forest**:
  - **AUPRC**: 0.955
  - **F1**: 0.883
  - **Precision**: 0.886
  - **Recall**: 0.881
- **SVC**:
  - **AUPRC**: 0.947
  - **F1**: 0.867
  - **Precision**: 0.878
  - **Recall**: 0.856
- **XGBoost**:
  - **AUPRC**: 0.957
  - **F1**: 0.889
  - **Precision**: 0.887
  - **Recall**: 0.891

## Results
- The **XGBoost** model achieved the best performance with high precision and recall for medal prediction, making it the most suitable for identifying potential sponsorship candidates.
- Key insights:
  - Age and event category significantly impact medal likelihood.
  - Higher consistency and performance are observed in long-term participants and certain sports.

## Recommendations
1. **Early Warning System** - Track athlete performance patterns to proactively identify sponsorship candidates.
2. **Targeted Sponsorship** - Focus on athletes in high-yield demographics and sports with strong medal prospects.
3. **Community Engagement** - Consider sponsorship initiatives that align with Kellogg's brand and athlete community involvement.

# CS534 ML Final Project: Seizure Detection Seizure Prediction
## Overview

This project focuses on the development and evaluation of machine learning models for seizure detection and prediction using Electroencephalogram (EEG) data. Epilepsy, a neurological disorder, affects millions worldwide, and automated seizure detection systems are crucial for improving patient outcomes. This study explores various machine learning techniques, including Random Forest, Long Short-Term Memory (LSTM) networks, and Support Vector Machines (SVM), to classify seizure events and predict the onset of seizures.

## Objectives

**Seizure Detection:** Classify EEG clips as either seizure (ictal) or non-seizure (interictal) using machine learning models.

**Seizure Prediction:** Predict the likelihood of an upcoming seizure by distinguishing between preictal and interictal EEG states.

## Dataset

**Source:** The data used in this project is sourced from the University of Pennsylvania and the Mayo Clinic.

**Structure:**

&nbsp;&nbsp;&nbsp;&nbsp;**Seizure Detection:** EEG clips labeled as "Ictal" or "Interictal."   
&nbsp;&nbsp;&nbsp;&nbsp;**Seizure Prediction:** EEG clips labeled as "Preictal" (before seizure) or "Interictal."   

## Feature Selection

**Frequency Domain:**

&nbsp;&nbsp;&nbsp;&nbsp;**· Fast Fourier Transform (FFT):** Used to convert EEG signals from the time domain to the frequency domain, focusing on frequencies between 1-47Hz.
&nbsp;&nbsp;&nbsp;&nbsp;**· Correlation Coefficients:** Calculated in both time and frequency domains.
&nbsp;&nbsp;&nbsp;&nbsp;**· Eigenvalues:** Extracted from the correlation matrix to capture the variance in EEG signals.
&nbsp;&nbsp;&nbsp;&nbsp;**· Time Domain:** Similar techniques applied as in the frequency domain, focusing on capturing temporal features of the EEG signals.

## Models Used

    Random Forest:
        Achieved the highest accuracy in seizure detection with a combination of FFT and correlation features.
    Support Vector Machine (SVM):
        Showed strong performance, particularly with frequency correlation features, achieving high precision.
    Long Short-Term Memory (LSTM):
        Explored for its ability to handle sequential data, though performance was lower due to model complexity and resource constraints.
    Linear and Logistic Regression:
        Applied in seizure prediction, with Logistic Regression outperforming Linear Regression, particularly with frequency correlation features.

Model Evaluation

    Metrics: Accuracy, Recall, Confusion Matrix, and F1 Score were used to evaluate model performance.
    Results:
        Random Forest: Best overall performance in seizure detection with nearly 97% accuracy.
        SVM: High accuracy (~90%) but lower F1 scores due to high false negatives.
        LSTM: Lower accuracy (~70%), limited by model complexity.
        Logistic Regression: Outperformed Linear Regression in seizure prediction, particularly with frequency correlation features.

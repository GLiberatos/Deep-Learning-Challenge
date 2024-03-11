# Deep Learning Challenge - Module 21

## Overview
This project tackles the task of predicting applicant success in securing funding using machine learning techniques, particularly employing a Keras neural network model in Python with TensorFlow, Scikit-learn, and Pandas. The aim is to train and assess a model that can effectively determine whether an applicant would be successful if granted funding based on various input variables.

## Analysis Summary
The analysis revolves around using available data to build a predictive model for assessing applicant success upon receiving funding. The model primarily focuses on binary classification, categorizing applicants as either successful (1) or unsuccessful (0). The predictor variables utilized in this analysis include application type, affiliation, classification, use case, organization type, status, income amount, special considerations, and ask amount.

## Results
### Data Processing
- Target Variable: IS_SUCCESSFUL
- Feature Variables: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, ASK_AMT
- Variables Removed: EIN, NAME

### Model Compilation, Training, and Evaluation
- Neural Network Configuration:
  - 110 neurons distributed across 2 layers
  - Activation Function: ReLU
- Target Model Performance: Achieved 75% accuracy after optimizations.
- Steps Taken to Enhance Model Performance:
  - Identified outliers in the ASK_AMT variable as a major issue and focused the model on lower ask amounts (< $25,000) for better accuracy.
  - Explored techniques such as increased binning, adjusting neuron count, changing optimizers, updating epochs, and modifying loss compilers.

## Summary
While the model achieved a 75% accuracy rate, it's deemed insufficient given the diverse range of ask amounts present in the data. Further research is warranted, especially considering the significant disparity between ask amounts, ranging from thousands to billions of dollars. Tailoring the model to different ask amount categories may lead to improved performance.

## References
- Sklearn Documentation: [Link](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)
- TensorFlow Documentation: [Link](https://www.tensorflow.org/learn)
- ChatGPT for coding assistance: [Link](https://chat.openai.com/)
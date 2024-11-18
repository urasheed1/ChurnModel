# Customer Churn Prediction App

This repository contains a comprehensive solution for predicting customer churn using machine learning models and deploying the predictions via a Streamlit-based web application. The solution includes scripts for training models, generating explanations for predictions, and creating personalized emails to retain customers.

---

## Project Structure

- **MachineLearningChurnModel.ipynb**: Script for training and saving machine learning models to `.pkl` files.
- **main.py**: Streamlit-based web application for customer churn prediction, explanations, and email generation.
- **utils.py**: Utility functions for enhancing visualization and interactivity in the web app.
- **churn.csv**: Dataset containing customer data for training and testing models.

---

## How to Use

### 1. Prepare Your Models

The **MachineLearningChurnModel.ipynb** script trains and saves machine learning models. Follow these steps:

1. **Open the Notebook**:
   - Load `MachineLearningChurnModel.ipynb` in Jupyter Notebook or Google Colab.
2. **Train the Models**:

   - Ensure the `churn.csv` dataset is in the same directory.
   - Run the cells in the notebook to preprocess the data, train multiple models, and evaluate their performance.

3. **Save the Models**:
   - The script will save the trained models as `.pkl` files, such as:
     - `xgb_model.pkl`
     - `nb_model.pkl`
     - `rf_model.pkl`
     - `voting_clf.pkl`
     - (and more)

---

### 2. Build the Web Application

Use the `main.py` script to create a Streamlit-based web application.

#### Requirements:

1. **Replit Setup**:

   - Create a project in Replit and upload `main.py`, `utils.py`, and the `.pkl` files.

2. **Install Dependencies**:

   - Add the following to a `requirements.txt` file:
     ```plaintext
     streamlit
     pandas
     numpy
     scikit-learn
     openai
     plotly
     ```

3. **Environment Variables**:
   - Create an account on [Groq](https://groq.com/) to obtain an API key.
   - Set the environment variable `GROQ_API_KEY` with your key in Replit.

#### Run the Application:

1. Start the Replit project.
2. Open the Replit URL in a browser.
3. Use the web app to:
   - Select a customer from the dropdown list.
   - Input customer details to simulate predictions.
   - Get a prediction on churn probability.
   - View an explanation for the prediction.
   - Generate a personalized email to retain the customer.

---

## Application Features

1. **Predict Customer Churn**:

   - Predicts the likelihood of a customer churning using multiple pre-trained models.
   - Displays individual model probabilities and an average probability.

2. **Explain Predictions**:

   - Provides natural language explanations for predictions using Groq's Llama model.

3. **Generate Personalized Emails**:

   - Creates a tailored email based on the customer's churn probability, incentivizing them to stay with the bank.

4. **Interactive Dashboard**:
   - Allows users to explore customer data and simulate predictions dynamically.

---

## Prerequisites

1. Python 3.8+
2. Groq API key.
3. Streamlit installed on your local machine or a platform like Replit.

---

## Future Enhancements

- Add more visualization for model performance.
- Support batch predictions for multiple customers.
- Enhance the email generation logic with more customer-specific data.

---

Feel free to explore and extend the project! Let me know if you have any questions or need additional help.

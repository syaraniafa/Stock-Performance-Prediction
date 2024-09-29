# Stock Performance Prediction for Company "X" - Deep Learning Project

## Overview
This project is part of the UAS (Final Assessment) for Deep Learning. The task simulates a real-world scenario where you are an AI Engineer working in the finance sector, tasked with predicting the stock performance of Company "X" using a provided time series dataset (X.csv).

The project involves developing a deep learning architecture to forecast the stock's closing price, focusing on the Date and Close columns. Several key tasks such as data preprocessing, architectural design, evaluation, and comparison are required to ensure accurate predictions.

## Dataset
- Filename: X.csv
- Columns of Interest:
  - Date: The date of the stock price data.
  - Close: The closing price of the stock on that date.

## Key Tasks
1. **Data Exploration and Preprocessing**
Before building any deep learning model, we conduct initial exploration to understand the dataset and address challenges inherent to time series data, such as:
    - Handling missing values.
    - Understanding trends or seasonality in the data. <br>

Preprocessing steps include:
Time Series Splitting: The dataset is split into input-output pairs with a window size of 5 and horizon of 1. This means for every 5 consecutive days of input data, the model predicts the stock closing price for the next day (horizon = 1).

2. **Data Partitioning**
To ensure the model generalizes well, the data is split into three distinct sets:
    - Train Set: 80% of the data.
    - Validation Set: 10% of the data.
    - Test Set: 10% of the data.

3. **Model Architecture**

    a. **Base Model**
  The first architecture is constructed based on Table 1 (provided in the project notebook), which acts as the foundational deep learning model.
  
    b. **Sequential Self-Attention Mechanism**
  An advanced architecture is then created by adding a **Sequential Self-Attention Mechanism** to enhance the model's ability to focus on important parts of the input sequence. <br>
    **Explanation of Self-Attention**: This mechanism enables the model to weigh the importance of each time step when making predictions, allowing it to capture long-term dependencies in the stock data more effectively than traditional sequential models.

4. **Model Evalution**
The trained models are evaluated on the test set using the following Evaluation metrics:
    - Mean Absolute Error (MAE): Chosen due to its straightforward interpretation in terms of the actual price difference.
    - Mean Squared Error (MSE): Useful for penalizing larger errors, ensuring the model captures significant deviations in stock price.
  Justification for these metrics is provided in the notebook.

5.  **Results and Analysis**
The results obtained from both models (1c and 1d) are thoroughly analyzed and compared:
  - Prediction Results: The predictions from the base model and the model with the self-attention mechanism are compared to the actual stock prices.
  - Line Chart Comparison: A line chart visualizes the performance of both models against actual closing prices to clearly depict the differences in prediction accuracy.

## Conclusion
This project demonstrates the ability to build and enhance deep learning architectures for time series forecasting. By utilizing Sequential Self-Attention and standard architectures, the model's performance in predicting stock prices is evaluated and compared, providing insights into the advantages of more complex models in financial forecasting.

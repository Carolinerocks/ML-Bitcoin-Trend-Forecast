# ML-Bitcoin-Trend-Prediction

**1. Project Overview**

This project focuses on forecasting the direction of Bitcoin price movements (rise or fall) using a machine learning model. Instead of predicting exact prices, the emphasis is on identifying whether the price will increase the next day, which is crucial for making informed investment decisions.

The model labels daily price movement as:

- 1: Price will rise.

- 0: Price will fall.

**2. Objectives**

- Analyze historical Bitcoin price data to identify patterns and trends.

- Build a machine learning model to predict daily price direction.

- Evaluate the model's performance using precision as the key metric, given its importance in minimizing false positives for financial decision-making.

**3. Data Source**

The historical price data for Bitcoin was obtained from Yahoo Finance.

**4. Methods: Machine Learning Model**

Random Forest Classifier was chosen as the machine learning model for this project for several reasons:

- The project focuses on predicting the direction of price movement (up or down) rather than exact price values, making Random Forest—a classification algorithm—a suitable choice.

- Random Forest can handle nonlinear relationships and complex feature interactions effectively, which are prevalent in financial data like Bitcoin.

- It is robust to overfitting, as it averages predictions from multiple decision trees, which is crucial in volatile and noisy markets.

- Compared to other models like SVM or deep learning, Random Forest provides feature importance scores, allowing for better interpretability and insights into the most significant predictors.

- It requires less parameter tuning than models like Gradient Boosting (e.g., XGBoost), making it faster to implement and experiment with.

- Random Forest efficiently handles high-dimensional data without requiring extensive preprocessing, such as normalization or scaling, simplifying the workflow.

**5. Evaluation**

- Backtesting: Used rolling windows to train and test the model iteratively on historical data.

- Key Metric: Precision score, prioritizing correct predictions of upward trends to reduce financial risk.

**6. Results**

- Initial Precision: The first calculation yielded a precision score of 43.75%, slightly below random guessing (50%).

- Enhanced Model Precision:

  - Improved to 51.61% after introducing the base predictors.
  - Further increased to 56.44% by adding enhanced features and optimizing model parameters.

- Insights:
  - The improvement from the first model to the final model represents a significant gain of approximately 29.01% in precision.
  - Even modest predictive accuracy above 50% holds significant value in volatile markets like Bitcoin.

**7. Conclusion**

This project demonstrates the potential of using machine learning to predict Bitcoin price movements. While the precision score of 56.44% may seem moderate, it reflects the realistic challenges of financial forecasting and provides a practical edge in decision-making.

**8. Technologies Used**

- Python Libraries:

  - pandas and matplotlib for data preprocessing and visualization.
  - sklearn for implementing and evaluating the Random Forest model.
  - yfinance for fetching historical Bitcoin data.

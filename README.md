# Evaluation on Predictive Portfolios using Deep Learning Models
This project explores the application of deep learning models in predicting stock prices and constructing optimized investment portfolios. The project's goal is to analyze whether the use of deep learning models can improve portfolio performance compared to traditional portfolio optimization techniques.

## 1. Introduction
The hypothesis of the project is that deep learning models are effective in predicting stock prices, which can lead to improved portfolio performance. However, financial data is sparse and complex, making it challenging for deep learning models to outperform traditional models. This project aims to evaluate the effectiveness of deep learning models and their impact on portfolio optimization.

## 2. Data Collection and Preprocessing
- Selected 20 stocks from 8 different sectors over a period of nearly 5 years, focusing on pre-2020 data to avoid COVID-19 effects
- Preprocessed training data using log returns and Winsorization technique for more robust mean and covariance calculations
- Visualized log returns for each stock to understand the data distribution
- Compared original and Winsorized mean and covariance of stocks to highlight the impact of preprocessing

## 3. Traditional Portfolios
- Developed helper functions for Sharpe Ratio (SR) and Relative Risk Contribution (RRC) calculations
- Constructed Heuristic Portfolios: Equally Weighted Portfolio (EWP) as a simple benchmark and Quintile Portfolio (QP)
- Implemented Markowitz's Portfolio Theory: Maximum Sharpe Ratio Portfolio (MSRP) for optimal risk-adjusted returns
- Designed Risk-Based Portfolios: Risk Parity Portfolio (RPP) with Convex Formulation and Mean-CVaR portfolio (MCVaRP) for risk diversification
- Visualized the allocations, RRCs, and SRs for each portfolio

## 4. Backtesting and Evaluation
- Evaluated the performance of the traditional portfolios using metrics such as cumulative returns, drawdown, Alpha, and Beta
- Performed backtesting on both historical and synthetic data to validate the model's performance
- Visualized the evaluation results, setting EWP as a benchmark with Alpha = 0 and Beta = 1

## 5. Deep Learning Models
- Further split the train_data into 70% X_train, y_train and 30% X_test, y_test for deep learning models
- Created sequences (y) with specified window size for time-series data
- Implemented Deep Learning Models: Gated Recurrent Unit (GRU), Long Short-Term Memory (LSTM), and Transformer, addressing the sequential nature of financial data
- Trained and manually tuned the hyperparameters, aiming to match X_test, achieve a good-looking loss curve, and reach an MAE ≤ 150
- Used the best-performing models to generate predicted_test_data for backtesting

## 6. Experiment
- Conducted extensive training for all three deep learning models through iterative processes
- Explored various hyperparameter combinations in a separate playground section for fine-tuning
- Visualized the average results using only the models with MAE ≤ 150 to understand the impact of deep learning models on portfolio performance

## 7. Conclusion
The project concluded that deep learning models did not significantly improve portfolio performance compared to traditional models. The predictive capability of the models was limited due to the complexity and sparsity of financial data. However, the project still provides valuable insights into the application of deep learning models in finance, and there is potential for improvement with advanced techniques such as enhanced data cleaning, feature engineering, and incorporating macroeconomic indicators.

## 8. Potential Improvements
- Enhanced data cleaning to reduce noises, such as de-trending, seasonality decomposition, or Principal Component Analysis (PCA)
- Advanced feature engineering techniques like rolling averages, time-based aggregations, and technical indicators
- Experimenting with advanced deep learning model designs, such as ensemble learning, different architectures, or attention mechanisms
- Incorporating macroeconomic indicators, such as inflation rates, GDP growth, and market sentiment, to better understand the underlying trends and factors that influence stock prices

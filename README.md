# Stock-Price-Prediction-LSTM-

This repository contains an advanced Deep Learning project focused on predicting the closing prices of Microsoft (MSFT) stock using a **Stacked Long Short-Term Memory (LSTM)** model.

The project demonstrates end-to-end time-series processing, from data sequencing to model deployment and evaluation using key financial metrics.

## Key Project Highlights
* **Domain:** Finance, Time-Series Forecasting.
* **Architecture:** Stacked LSTM (2 layers, 50 units each).
* **Input Sequencing:** Data was prepared using a **60-day lookback window** to train the model on sequential dependencies.

## Performance & Evaluation

The model was rigorously evaluated on the unseen test data. The minimal gap between training loss and validation loss confirmed a highly stable fit.

| Metric | Value | Interpretation |
| :--- | :--- | :--- |
| **Model Fit (Val. Loss)** | $1.8408e-05$ | Excellent fit, indicating low variance. |
| **MAE (Mean Absolute Error)** | **$7.14$ USD** | Average deviation from the actual closing price. |
| **RMSE (Root Mean Squared Error)** | $12.14$ USD | Overall standard deviation of prediction errors. |

## Visual Analysis The plot compares the Actual Price vs. the Predicted Price on the test set.

* The model **successfully captures the long-term trend** and overall movement.
* **Limitation:** A **prediction lag** is visible during periods of high volatility, a common challenge with standard LSTM architectures.

## Future Work
1.  **Transformer Implementation:** Replace the LSTM with a **Transformer-based model** to eliminate the temporal lag and better capture long-range dependencies in the time series.
2.  **Feature Augmentation:** Incorporate external features like trading **Volume, Volatility (ATR), or sentiment data** to improve context-aware predictions.

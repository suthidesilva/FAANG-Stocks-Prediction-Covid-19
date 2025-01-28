# Predicting FAANG Stock Prices During a Pandemic: Analysis and Results

## 1. Introduction
This project predicts the stock prices of FAANG companies during a simulated pandemic, similar to COVID-19, based on historical trends and economic factors. The analysis employs Linear Regression, Random Forest, and LSTM models to compare performance and generate predictions.

---

## 2. Dataset and Feature Engineering
**Dataset**: Historical FAANG stock price data during the COVID-19 pandemic.

**Features**:
- **Stock Metrics**: Open, High, Low, Close, Volume.
- **Derived Metrics**: 5-day and 30-day moving averages, daily price range, percentage price change.
- **Simulated Pandemic Conditions**: Adjusted trading volume (+50%) and percentage price changes (+20%) to reflect increased volatility.

---

## 3. Models Used
### **Linear Regression**
- **Purpose**: Provides a simple baseline to understand linear relationships between features and the target variable.

### **Random Forest Regressor**
- **Purpose**: Captures non-linear relationships and ranks feature importance to improve prediction accuracy.

### **Long Short-Term Memory (LSTM)**
- **Purpose**: Designed for sequential time-series data, capturing temporal dependencies for more robust predictions.

---

## 4. Model Evaluation and Performance

| Model                | Mean Squared Error (MSE) | R² Score |
|----------------------|--------------------------|------------|
| Linear Regression    | `{{linear_mse}}`        | `{{linear_r2}}` |
| Random Forest        | `{{rf_mse}}`            | `{{rf_r2}}` |
| LSTM                 | `{{lstm_mse}}`          | `{{lstm_r2}}` |

**Best Model**: The model with the highest R² score is chosen for prediction.

---

## 5. Prediction Results
### **Predicted Prices During a Simulated Pandemic**
A visualization of the predicted stock prices for FAANG companies under simulated pandemic conditions:

```python
plt.figure(figsize=(12, 6))
for company, group in df.groupby('Name'):
    plt.plot(group['Date'], group['Predicted_Pandemic_Prices'], label=company)
plt.title('Predicted Pandemic Prices for FAANG Companies')
plt.xlabel('Date')
plt.ylabel('Predicted Prices')
plt.legend()
plt.grid(axis='both', linestyle='--', alpha=0.7)
plt.show()
```

### **Sample Predictions**
| Company | Date       | Actual Close Price | Predicted Pandemic Price |
|---------|------------|--------------------|--------------------------|
| `{{sample_company_1}}` | `{{sample_date_1}}` | `{{actual_close_1}}`     | `{{predicted_price_1}}`   |
| `{{sample_company_2}}` | `{{sample_date_2}}` | `{{actual_close_2}}`     | `{{predicted_price_2}}`   |

---

## 6. Conclusion
The results demonstrate the ability of supervised learning models to predict FAANG stock prices under pandemic-like conditions. LSTM models show particular promise for capturing temporal dependencies in stock price data.

---

## 7. References
- Historical stock data sourced from publicly available datasets.
- COVID-19 case data and economic indicators integrated for enhanced feature engineering.

---

## 8. Appendix
The complete code for data preprocessing, model training, evaluation, and prediction can be found [here](#).

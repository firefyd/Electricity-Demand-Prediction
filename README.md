# Electricity-Demand-Prediction
Accurate consumption forecasting is essential in optimising grid operations, integrating renewable energy sources, reducing costs, and informing decision-making for a range of stakeholders—including energy providers (e.g., AGL, Origin), the Australian Energy Market Operator (AEMO), policymakers, and consumers.

This report explores a data science approach to forecasting electricity demand, with the intent to identify the most accurate predictive method and assess whether temperature is the most influential variable in determining electricity demand.

First, a literature review explores traditional time series models like Holt-Winters and SARIMA, and contrasts them with advanced machine learning methods, particularly Long Short-Term Memory (LSTM) networks. Key challenges in modelling electricity consumption are addressed through feature engineering, such as seasonality, volatility, and the influence of exogenous factors like weather and holidays.

Using five-minute interval data from the Bankstown area, the modelling evaluates three predictive models explored in the literature review: Holt-Winters, SARIMA, and LSTM. The dataset includes historical demand, forecast demand, and temperature, spanning from 2010 to 2020.

The Holt-Winters model, limited by its inability to include external variables, performed poorly with a mean absolute percentage error (MAPE) of 15.5%. SARIMA, which incorporated temperature and calendar variables, achieved a significantly better MAPE of 5.2%. However, the best results were obtained with LSTM networks. A 48-hour input window LSTM model achieved the best balance of performance and efficiency, producing a MAPE of 3.23% and an R² of 0.92.

Although the 72-hour windowed LSTM achieved a marginally lower MAPE of 3.22%, the 48-hour model was preferred due to its better computational efficiency, smoother learning curve, and comparable accuracy. The 48-hour model displayed lower training complexity, faster convergence, and smaller gaps between training and validation loss, indicating stronger generalisation and practical suitability.

The findings confirm that temperature is a strong predictor of electricity demand, particularly when squared to capture non-linear effects, but it is most effective when used alongside engineered features such as lagged demand and time-based indicators. The report concludes that LSTM offers the best balance of predictive accuracy and scalability, recommending it as the preferred approach for stakeholders seeking high-performing, real-time forecasting solutions.

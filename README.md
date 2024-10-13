The following code is an alternative to avoid manual hyper-tuning and provide a batch process that can do so automatically.

While performing the different functions, I set up a max number of attempts so we can rule out the possibility of creating an infinite loop.

###############

Key takeaways:

###############

1)Python hyper-opt library will not provide us the optimal minimum of the gradient function but the local minima, which is enough to provide decent hyperparameters.

2)Date diff was the simplest and most efficient transformation approach I used to deal with stationarity. I realize that if I squeeze the p_value of ADF Fuller threshold, I can obtain better predictions.

3)I set up the optimization target for R2_Square but it is even more recommended RSME so you can change the target to follow that approach.

4)I set up the Jupiter workflow in a workflow fashion so the model can easily be retrained if requested.

###############

The Jupyter Notebook naive_forecaster_approach_02.ipynb is primarily focused on time series forecasting using a NaiveForecaster model. Here are the key components:

Library Imports: The notebook imports several libraries such as numpy, pandas, sktime, statsmodels, matplotlib, seaborn, and hyperopt for data manipulation, forecasting, plotting, and optimization.
DataWizard Class: This class handles various data operations:
Initialization: Sets up the model folder and suppresses warnings.
Data Loading: Loads and filters data from a CSV file.
Data Transformation: Prepares data for machine learning models.
Data Splitting: Splits data into training and testing sets.
ADF Test: Evaluates and transforms the time series data to achieve stationarity.
Bayesian Optimization: Optimizes the NaiveForecaster model using hyperopt to maximize the R² score.
Model Fitting and Prediction: Fits and predicts multiple departments using the optimized model.
Decompression: Decompresses the time series data to match the predicted values.
Plotting: Plots the forecasted vs. real values and prints performance metrics.
Execution Cells: The notebook contains cells that instantiate the DataWizard class, load data, perform ADF tests, and optimize the model.

Should you have any constructive input, please do no hesitate to contact me bpiscoya2020@gmail.com

Best Regards



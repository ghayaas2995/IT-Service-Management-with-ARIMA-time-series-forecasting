# IT-Service-Management-with-ARIMA-time-series-forecasting

ABC Tech is a mid-size organisation operation in IT-enabled business segment over a decade. On an average ABC Tech receives 22-25k IT incidents/tickets , which were handled to best practice ITIL framework with incident management, problem management, change management and configuration management processes. These ITIL practices attained matured process level and a recent audit confirmed that further improvement initiatives may not yield return of investment. Therefore, Machine learning looks prospective to improve ITSM processes through prediction and automation.

![image](https://user-images.githubusercontent.com/74657588/185484696-59e0537f-2cac-4e32-b719-66827c8c7b0f.png)

Dataset: 

The company incident volume data was sourced from company's MySQL database. It was a timeseries data having over 46000 ticket information and 25 features. The following analysis and tasks were performed to the dataset.

Data Engineering:

Checked the missing values in each feature and replaced all other kinds of missing value representations like "NS", blanks to a uniform NaN value. Performed univariate imputations and imputed all variables with most suitable and logically reasonable value (bfill, ffill, mode, 0 and more)

Handled date time variables using datetime package in Python. Changes the object data format to datetime, imputed missing values in datetime variables by performing time delta calculations. 

Created new features in the dataset like "First touch resolution", "Reopened yes or no" which indicates if the ticket was resolved at it's first assignment or if a ticket was reopened or not by researching about ITSM practices and researching domain knowledge.

Data Analysis:

Explored indepth distribution of all variables, obtained summary statistics, plotted statistical graphs like histograms, scatter plots, bar graphs and boxplots to analyze distribution of variables, analyzed continuous and discrete numerical features, analyzed categorical features for determining cardinality and checked against the response variable - Priority, to determine factors contributing to high priority tickets. Label encoded categorical features and scaled numerical features wirth MinMaxScaler

Model building:

Built a XG Boost model with features selected from an extra tree classifier feature importance selection technique and predicted high priority tickets with 98% accuracy. Used SMOTE to treat imbalanced data and performed hyper parameter tuning with grid search to improvise model performance.

ARIMA Model - Built an ARIMA (Auto Regressive Integrated Moving Average) model to forecast the quarterly and annual incident volume in each category of ITSM. Checked for stationarity of variables using Adfuller test and to satisfy the stationarity assumption in time series forecasting. Plotted autocorrelation and partial autocorrelation plots to determine p,d,q values, created a base forecasting model and evaluated and tuned p,d,q values to obtain best forecasting with ARIMA model



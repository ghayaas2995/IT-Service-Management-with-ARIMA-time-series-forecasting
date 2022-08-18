# IT-Service-Management-with-ARIMA-time-series-forecasting

ABC Tech is a mid-size organisation operation in IT-enabled business segment over a decade. On an average ABC Tech receives 22-25k IT incidents/tickets , which were handled to best practice ITIL framework with incident management, problem management, change management and configuration management processes. These ITIL practices attained matured process level and a recent audit confirmed that further improvement initiatives may not yield return of investment. Therefore, Machine learning looks prospective to improve ITSM processes through prediction and automation.

Dataset: 

The company incident volume data was sourced from company's MySQL database. It was a timeseries data having over 46000 ticket information and 25 features. The following analysis and tasks were performed to the dataset.

Data Engineering:

Checked the missing values in each feature and replaced all other kinds of missing value representations like "NS", blanks to a uniform NaN value. Performed univariate imputations and imputed all variables with most suitable and logically reasonable value (bfill, ffill, mode, 0 and more)

Handled date time variables using datetime package in Python. Changes the object data format to datetime, imputed missing values in datetime variables by performing time delta calculations. 

Created new features in the dataset like "First touch resolution", "Reopened yes or no" which indicates if the ticket was resolved at it's first assignment or if a ticket was reopened or not by researching about ITSM practices and researching domain knowledge.

Visualized distribution of variables using statistical charts and cleaned outliers.



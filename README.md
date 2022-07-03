# *Forecasting Net Prophet*
---

## Forecasting Net Prophet
This project covers the use of the fbProphet to make predictions about search trends and stock prices based on historical data. 

>"Todays forecast is sunny skies and clear projections"

## Technologies 

This project uses Pandas, Hvplot, and fbprophet libraries to create dataframes, perform data forecasts, and plot graphical interpretations of data. 

[pandas](https://github.com/pandas-dev/pandas)
[HVplot](https://github.com/holoviz/hvplot)
[SKLearn](https://github.com/facebook/prophet)

### Installation Guide

In order to use this program please import and utilize the following libraries and dependencies: 

```python
import pandas as pd
import numpy as np
import holoviews as hv
from fbprophet import Prophet
import hvplot.pandas
from pathlib import Path
import datetime as dt
%matplotlib inline
```

## Usage 
the following blocks of code are fundamental in executing the program. 

```python 
df.groupby().mean().hvplot(title=)
```
This groups the dataframe by a specific time or index to allow plotting of data. 
```python
 df.index.isocalendar().week
```
This command indexes the dataframe by a weekly time bracket. The timeframe can be hours, days, weeks, etc.   
```python
df_combined = pd.concat([df_1, df_2], axis=1).dropna()
```
This command joins two seperate dataframes to allow the prophet library to create forecasts. Null values are dropped.  

```python
df_trends = Prophet()
```
This command instantiates the prophet library. 

```python
df_trends.fit(df)
```
This command fits the original dataframe into the prophet model for analysis. 

```python
forecast_df = df_model.predict(df_future_trends)
```
This command creates the prediction based off the fitted historical data. 

```python
forecast_df[['yhat', 'yhat_lower', 'yhat_upper']].iloc[-24:,:].hvplot(title="")
```

This plot command will display the selected columns from the future dataframe projections with an hvplot. 


![<alt text>](https://i.postimg.cc/XJdLvBcG/Screen-Shot-2022-07-03-at-11-45-15-AM.png)

## Contributors

Jeffrey J. Wiley Jr

## License

MIT



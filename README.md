# Price_Optimisation_Sample
Sample Files
Price Optimization
Price optimization is the use of mathematical analysis by a company to determine how customers will respond to different prices for its products and services through different channels. It is also used to determine the prices that the company determines will best meet its objectives such as maximizing operating profit. The data used in price optimization includes operating costs, inventories and historic prices and sales. Price optimization practice has been implemented in industries including retail, banking, airlines, casinos, hotels, car rental, cruise lines and insurance. (https://en.wikipedia.org/wiki/Price_optimization)

Dataset
You can download an initial dataset from [Dunnhumby](https://www.dunnhumby.com), we use dataset [Breakfast at the Frat](https://www.dunnhumby.com/sites/default/files/sourcefiles/dunnhumby_Breakfast-at-the-Frat.zip)



Snippet : 
import numpy as np
from datetime import datetime, timedelta
import pandas as pd

today = datetime.now().date()

start_date = today - timedelta(days=30)
date_range = pd.date_range(start=start_date, end=today, freq='D')

a = []
for date in date_range:
    path = f"/predictions/level=week/updated_dt={date.strftime('%d-%m-%y')}"
    spark_df = spark.read.parquet(path)
    pandas_df = spark_df.toPandas()
    n = pandas_df.nunique(axis=0)
    a.append(n[0])

print(a)
print(np.mean(a))


file_name = f"data_{today.strftime('%Y-%m-%d')}.csv"
pd.DataFrame({'value': a}).to_csv(file_name, index=False)
print(f"Data saved to {file_name}")

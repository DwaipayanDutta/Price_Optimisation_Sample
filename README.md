# Breakfast at the Frat

## 📦 What's Inside?
This dataset provides detailed sales and promotion information for five products across three brands and four categories (mouthwash, pretzels, frozen pizza, and boxed cereal) over a span of 156 weeks. It includes:

- **📊 Unit Sales**: Units sold, households, visits, and spend data by product, store, and week.
- **💲 Base Price & Shelf Price**: Base price and shelf price to determine product discounts.
- **🎯 Promotional Support**: Details on promotional support (e.g., sale tags, in-store displays) when applicable.

## 🎯 What's It For?
This dataset is ideal for time series analyses, including:

- **🔍 Price Sensitivity Analysis**: Examine how changes in price affect sales.
- **📈 Promotional Effectiveness Analysis**: Assess the impact of promotions on sales.
- **📊 Comparative Analysis**: Compare results across products, categories, or store geographies.

## 📋 Data Dictionary

| Column Name  | Description                                                                 |
|--------------|-----------------------------------------------------------------------------|
| CATEGORY     | The product category (mouthwash, pretzels, frozen pizza, boxed cereal)      |
| BRAND        | The brand name of the product                                               |
| PRODUCT      | The specific product name                                                   |
| STORE        | The store ID where the product was sold                                     |
| WEEK         | The week number (1-156)                                                    |
| UNITS        | The number of units sold                                                    |
| HOUSEHOLDS   | The number of households that purchased the product                         |
| VISITS       | The number of store visits where the product was purchased                  |
| SPEND        | The total dollar amount spent on the product                                |
| BASE_PRICE   | The regular shelf price of the product                                      |
| SHELF_PRICE  | The price the product was sold at, which may be lower than BASE_PRICE if it was on promotion |
| PROMOTION    | Indicator of promotional support (e.g., sale tag, in-store display)        |

## 💻 Usage Example

```python
import pandas as pd
# Load the data
%%time
data=pd.ExcelFile('Breakfast_at_the_Frat.xlsx')
# Explore the first few rows
print(data.head())

# reading all sheet
stores=breakfast.parse(sheet_name=1,header=1,usecols=range(9))
products=breakfast.parse(sheet_name=2,header=1, usecols=range(6))
transaction=breakfast.parse(sheet_name=3,header=1,usecols=range(12))
```
## 📦 Dataset
You can download an initial dataset from [Dunnhumby](https://www.dunnhumby.com), we use dataset [Breakfast at the Frat](https://www.dunnhumby.com/source-files)
Feel free to reach out if you have any questions or need further assistance! 🚀

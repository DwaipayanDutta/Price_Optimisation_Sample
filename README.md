# Price_Optimisation_Sample
Sample Files
Price Optimization
Price optimization is the use of mathematical analysis by a company to determine how customers will respond to different prices for its products and services through different channels. It is also used to determine the prices that the company determines will best meet its objectives such as maximizing operating profit. The data used in price optimization includes operating costs, inventories and historic prices and sales. Price optimization practice has been implemented in industries including retail, banking, airlines, casinos, hotels, car rental, cruise lines and insurance. (https://en.wikipedia.org/wiki/Price_optimization)

Dataset
You can download an initial dataset from [Dunnhumby](https://www.dunnhumby.com), we use dataset [Breakfast at the Frat](https://www.dunnhumby.com/sites/default/files/sourcefiles/dunnhumby_Breakfast-at-the-Frat.zip)



Snippet : 
    def check_within_20_percent(df, column_name, target_value):
        lower_bound = target_value * 0.8
        upper_bound = target_value * 1.2
        
        return (df[column_name] >= lower_bound) & (df[column_name] <= upper_bound)

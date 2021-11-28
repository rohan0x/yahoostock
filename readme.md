# yahoostock
 A package designed to scrape data from Yahoo Finance.

## Installation
The most simple installation method is through PIP.
```
pip install yahoostock
```
The PyPI page can be found [here](https://pypi.org/project/yahoostock/).

## Usage
Use the following code to see a list of useful methods.
```py
from yahoostock import yahoo
print(dir(yahoo))
```
Note that each method accepts a stock ticker as a single parameter and returns a float with the specified statistic.

Here's an example:
```py
from yahoostock import yahoo

stock_name = "GOOGL"

function_list = [
    yahoo.get_price,
    yahoo.get_open,
    yahoo.get_previous_close,
    yahoo.get_change,
    yahoo.get_percent_change
]

for function in function_list:
    # prints current price($), opening price (%), previous closing price ($),
    # change in price ($), and relative change (%)
    print(function(stock_name))
```

# stock-sentiment

Tracking ethereum with different textual data sources to try to predict the stock
https://web.stanford.edu/class/cs224n/reports/final_reports/report030.pdf

https://medium.com/@yiaktan/using-nlp-and-deep-learning-to-predict-the-stock-market-64eb9229e102

https://www.reddit.com/r/ethereum/

news articles api with python:
https://newsapi.org/docs/client-libraries/python

stock market prices from yfinance
https://blog.quantinsti.com/historical-market-data-python-api/

## setup venv

for mac:

<pre><code>bash: python3 -m venv stock_hasan</code></pre>
<pre><code>bash: source stock_hasan/bin/activate</code></pre>
<pre><code>bash: pip install -r requirements.txt</code></pre>

## Some notes on development

reading from different news sources is a difficult challenge because of the formats of their pages, but news aggrigation sites have done this work for us. <br>
We also have the challenge of finding the right metrics to rank the news sources and their statements by. <br>
For example we could rank them purely on the textual data, and the sentiment that it has, but we might also want to factor in the amount of viewers that a particular outlet has, and we would somehow want to associate those viewers with stock traders, and also their actions given the news they look at. If we had some news outlet like the onion, which didn't convey real news, but had high viewership we may be fooled into thinking that people would listen to them. <br>
Can we ignore the viewership and the viewer and just look at the corrlation between the sentiment, the news and the price of stock? <br>
This is likely what we will be testing. I don't think it is a full picture, and I think it will lead to some pretty shoddy results as typical of a stock prediction algorithm. <br>

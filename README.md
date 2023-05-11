# Project_1

Importing libraries: We import the necessary libraries (matplotlib, numpy, seaborn, datetime) to
perform the analysis.

Loading environment variables: We load the environment variables from the .env file using the
load_dotenv function from the dotenv library.

Setting current amount of shares: We set the current amount of shares for five different stocks
in variables.

Setting API keys and creating API object: We configure the API keys and create an API object
for Alpaca. We store the Alpaca API key and secret in separate variables and utilise the REST
function from the alpaca_trade_api library to generate the API object.

Getting current closing prices: We calculate the current closing prices of the five stocks and
the S&P 500 from the Alpaca API using the get_bars function of the API object. We then
reorganise the DataFrame to separate the ticker data and concatenate them into a single
DataFrame, extracting the close prices for each stock into separate variables.

Getting historical data: We generate five years' worth of historical data for the same five stocks
and S&P 500 from the Alpaca API using the get_bars function of the API object. We reorganise
the DataFrame to separate the ticker data and extract the close prices for each stock into
separate variables. We then calculate the percentage change for each stock and drop the NaN
values. We concatenate the percentage change data into a single DataFrame.An image of this plot is shown here:

Daily returns: We calculate the daily returns for all portfolios and create a box plot to show the 
distribution of daily returns across the selected portfolios.
![Histogram](images/histogram.png)

Cumulative returns: We calculate and plot the cumulative returns over time, with colours 
indicating whether the returns were above or below the initial investment amount.

Daily standard deviations: We compute the daily standard deviations of all portfolios and print 
them, along with the rolling 21-day standard deviation for each portfolio plotted on a graph.

Annualised standard deviation: We calculate the annualised standard deviation using the daily
standard deviation and 252 trading days.

Correlation coefficients: We calculate the correlation coefficients between all portfolio pairs and
visualise them with a heat-map.

Beta values: We compute the beta values for the selected companies and display them in a bar
chart, showing how much the company's stock price moves relative to the broader market
represented by the SPY index.

Sharpe ratios: We compute the Sharpe ratios for each portfolio, indicating the risk-adjusted
return of each portfolio. We also compute annualised Sharpe ratios to provide a more
meaningful comparison of portfolios over time.

Scatter plot: Finally, we created a scatter plot to compare the daily standard 
deviation and Sharpe ratio of each portfolio, with the size of each point 
representing the average daily return for that portfolio. This plot can be used to 
compare the risk and return characteristics of each portfolio and identify the best 
investment options.

We then ran a 10 year Monte Carlo simulation on the historical data on these 
five stocks and created a Dataframe for the output. showing the combined 
returns over 10 years of all these stocks. This result was also depicted in a plot 
diagram as follows: 

A further DataFrame was created showing a summary of the statistics showing the 
mean, medium, minimum and maximum of returns for the combined portfolio as 
above.

Based on an assumed initial investment of $ 10,000, a progression of the cumulative 
returns of the portfolio was calculated. Following the summary statistics of this 
calculation, the folliowing result is printed: 'There is a 95% chance that an initial 
investment of $10,000 in the portfolio over the next year will end within in the range 
of $9445.81 and $80763.57.'

Further to the above, we have created widgets for users to input a selection of upto 3 
stocks with their weightages (adding upto 1). The user needs to further input their initial 
investment and click the button 'Submit'. The application will output in less than a 
minute, the following:

1) A concatenated DataFrame (DF)showing the daily returns of the selected custom 
portfolio and the individual stocks;

2) The above DF in visual representation in the forms of histogram plot, density plot 
and box plot;

3) Standard Deviation of the custom portfolio is calculated and represented in a 
rolling 21 day line plot diagram

4) Further covariance and beta is also calculated for the portfolio with reference to the other stocks and SPY.
The result is also shown in a bar chart presentation;

5) Next, the sharpre ratio is calculated for the custom portfolio and the other stocks and a visualisation in
the form of a sactter plot is presented

6) Lastly the Monte Carlo simulation is run and this process outputs a range of minimum and maximum
stock values with 95% confidence

A brief summary of the company and its business is also mentioned in the output


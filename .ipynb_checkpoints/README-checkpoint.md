# prophet-challenge

The code file to run will be <forecasting_net_prophet_edited.ipynb>.
The <forecasting_net_prophet.ipynb> file was a starter code file and was kept to use as reference and backup if the editing file was
lost or corrupted.

## Background
A simulation where I am a growth analyst at Mercado LibreLinks to an external site.. With over 200 million users, Mercado Libre is the most popular e-commerce site in Latin America. I've been tasked with analyzing the company's financial and user data in clever ways to make the company grow. I want to find out the ability to predict search traffic that can translate into the ability to successfully trade the stock.

There are 4 steps to the analytics of the data:

**Step 1:** Find unusual patterns in hourly Google search traffic.
**Step 2:** Mine the search traffic data for seasonality.
**Step 3:** Relate the search traffic to stock price patterns.
**Step 4:** Create a time series model with Prophet.

## Step 1: Find Unusual Patterns in Hourly Google Search Traffic

Check the Google search traffic for the company to see if it connects to any financial events at the company. Pick out any unusual patterns in the Google search data for the company, and connect them to the corporate financial events.

Read the search data into a DataFrame, and then slice the data to just the month of May 2020. (During this month, MercadoLibre released its quarterly financial results.) Visualize the results. Check if there are unusual patterns exist.

Calculate the total search traffic for the month, and then compare the value to the monthly median across all months.

How did the Google search traffic fare during the month that MercadoLibre released its financial results? 

## Step 2: Mine the Search Traffic Data for Seasonality

This step checks the hourly search data. It is to track and predict interest in the company and its platform for any time of day. This information allows the company to focus their marketing efforts around the times that have the most traffic. This will get a greater return on investment (ROI) from their marketing budget.

To do this we mine the search traffic data for predictable seasonal patterns of interest in the company.

Group the hourly search data to plot the average traffic by the hour of day. Check if the search traffic peaks at a certain time of day?

Group the hourly search data to plot the average traffic by the day of the week (for example, Monday vs. Friday). Check if the search traffic gets busiest during which day of the week.

Group the hourly search data to plot the average traffic by the week of the year. Check when the search traffic is the highest during the year.

## Step 3: Relate the Search Traffic to Stock Price Patterns

This step we want to know if there is any relationship between the search data and the company stock price exists.

Read in and plot the stock price data. Concatenate the stock price data to the search data in a single DataFrame.

Market events emerged during the year of 2020 that many companies found difficult. But, after the initial shock to global financial markets, new customers and revenue increased for e-commerce platforms. Slice the data to just the first half of 2020 (2020-01 to 2020-06 in the DataFrame), and then plot the data. 

Create a new column in the DataFrame named “Lagged Search Trends” that offsets, or shifts, the search traffic by one hour. 

Create two additional columns:
    “Stock Volatility”, which holds an exponentially weighted four-hour rolling average of the company’s stock volatility
    “Hourly Stock Return”, which holds the percent change of the company's stock price on an hourly basis

Now check if a predictable relationship exist between the lagged search traffic and the stock volatility or between the lagged search traffic and the stock price returns.

## Step 4: Create a Time Series Model with Prophet

This step we produce a time series model that analyzes and forecasts patterns in the hourly search data.

Set up the Google search data for a Prophet forecasting model.

After estimating the model, plot the forecast.

Plot the individual time series components of the model

The following are questions to be answered after plotting the individual time series components of the model:
    What time of day exhibits the greatest popularity?
    Which day of the week gets the most search traffic?
    What's the lowest point for search traffic in the calendar year?
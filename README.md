Stock and Revenue Data Dashboard
Overview
This project provides interactive dashboards for visualizing the historical stock prices and quarterly revenue of Tesla and GameStop. The stock price data is retrieved using the yfinance library, while the quarterly revenue data is extracted using web scraping. The visualization is done using plotly, allowing you to interactively explore the data.

The dashboard consists of two main sections:

Historical Share Price: A graph displaying Tesla's or GameStop's stock price over time.
Historical Revenue: A graph displaying the quarterly revenue of Tesla or GameStop.
This project allows users to compare the stock and revenue data for both companies side by side.

Technologies Used
yfinance: To retrieve historical stock price data from Yahoo Finance.
requests & BeautifulSoup: For scraping quarterly revenue data from a specific web page.
pandas: For managing and manipulating the data.
plotly: For creating interactive visualizations.
Project Structure
bash
Copy code
Stock-and-Revenue-Dashboard/
├── stock_revenue_dashboard.py    # Python script to retrieve data and generate the dashboard
├── README.md                    # Project overview and instructions

## Question 1: Use yfinance to Extract Stock DataUsing the `Ticker` function 
1. Enter the ticker symbol of the stock we want to extract data on to create a ticker object. The stock is Tesla and its ticker symbol is `TSLA`.

2. Using the ticker object and the function `history` extract stock information and save it in a dataframe named `tesla_data`. Set the `period` parameter to ` "max" ` so we get information for the maximum amount of time.

**Reset the index** using the `reset_index(inplace=True)` function on the tesla_data DataFrame and display the first five rows of the `tesla_data` dataframe using the `head` function.

## Question 2: Use Webscraping to Extract Tesla Revenue Data
1. Use the `requests` library to download the webpage https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/revenue.htm Save the text of the response as a variable named `html_data`.

2. Parse the html data using `beautiful_soup` using parser i.e `html5lib` or `html.parser`. Make sure to use the `html_data` with the content parameter as follow `html_data.content`
   
4. Using `BeautifulSoup` or the `read_html` function extract the table with `Tesla Revenue` and store it into a dataframe named `tesla_revenue`. The dataframe should have columns `Date` and `Revenue`.
   
## Question 3: Use yfinance to Extract Stock Data
1. Using the `Ticker` function enter the ticker symbol of the stock we want to extract data on to create a ticker object. The stock is GameStop and its ticker symbol is `GME`.
2. Using the ticker object and the function `history` extract stock information and save it in a dataframe named `gme_data`. Set the `period` parameter to ` "max" ` so we get information for the maximum amount of time.
   **Reset the index** using the `reset_index(inplace=True)` function on the gme_data DataFrame and display the first five rows of the `gme_data` dataframe using the `head` function.

## Question 4: Use Webscraping to Extract GME Revenue Data
1. Use the `requests` library to download the webpage https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/stock.html. Save the text of the response as a variable named `html_data_2`.
2. Parse the html data using `beautiful_soup` using parser i.e `html5lib` or `html.parser`.
3. Using `BeautifulSoup` or the `read_html` function extract the table with `GameStop Revenue` and store it into a dataframe named `gme_revenue`. The dataframe should have columns `Date` and `Revenue`. Make sure the comma and dollar sign is removed from the `Revenue` column.
4. Display the last five rows of the `gme_revenue` dataframe using the `tail` function.

## Question 5: Plot Tesla Stock Graph
1. Use the `make_graph` function to graph the Tesla Stock Data, also provide a title for the graph. Note the graph will only show data upto June 2021.

## Question 6: Plot GameStop Stock Graph
1. Use the `make_graph` function to graph the GameStop Stock Data, also provide a title for the graph. The structure to call the `make_graph` function is `make_graph(gme_data, gme_revenue, 'GameStop')`. Note the graph will only show data upto June 2021.




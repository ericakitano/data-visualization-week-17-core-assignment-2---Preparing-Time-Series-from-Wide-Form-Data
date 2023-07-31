# data visualization week 17 core assignment 2 - Preparing Time Series from Wide-Form Data
 

## Task


## Part 1
- First, you will prepare the dataset for time series analysis:
  - Load in the Zillow Home Value Index dataframe.
    - Note: it is a large file and may take a minute to load.
  - Filter the 4 largest cities into a new dataframe.
    - Tip: the "SizeRank" column has already ranked the cities by size. The larger the city, the smaller the rank value.
       - Therefore the 4 largest cities would have rank values of [0,1,2,3]
  - Melt the data to long-form and prepare it for time series analysis.
    - Convert the melted dates into datetime datatype.
    - Make the datetime column the index.
  - Resample the dataframe as monthly frequency, grouped by City.


## Part 2
- Once you've prepared the dataframe with the time series data for the 4 largest cities:
  - Plot the home values for all 4 cities. (Hint: use unstack)
    - Make sure to add a title and axis labels.
    - Reformat the y-axis ticks to use thousands of dollars with a "K" at the end. (e.g. "200K, 400K, etc")
       - Hint: use the FuncFormatter from matplotlib.
  - Answer the following 2 questions using pandas:
    - 1) Which City had the highest Typical Home Value at the end of 2008? Which had the least?
       - Hint: You can use the unstacked dataframe or use pd.IndexSlice with the multiindex. 
    - 2) How much did the home values change from November 2008 to December 2008 (in dollars)?
       - Hint: you can use .diff() to calculate the change in values

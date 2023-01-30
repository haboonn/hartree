##Pandas Approach
 
 
 My thesis for following the course of action I did was to utilize the power of pandas library in python to perform the requested data manipulation task in an efficient and simple way. I followed this course of action because it is an efficient way to perform the necessary transformations on the dataset. Joining the two dataframes on the "counter_party" column ensures that the "tier" column is included in the resulting dataframe. Grouping the dataframe by the "legal_entity", "counterparty", and "tier" columns makes it possible to aggregate the data by those columns. Finally, adding the total records provides a summarized view of the data that makes it easier to understand and analyze. Below is a step by step outline of how I approached this task. 


1. Import the pandas library to use dataframes
2.Create two dataframes, dataset1 and dataset2
3.Join the two dataframes on the "counter_party" column
4.Group the resulting dataframe by the "legal_entity", "counterparty", and "tier" columns
5.Use the "max" function on the "rating" column to find the maximum rating by counterparty
6.Use the "sum" function on the "value" column to find the sum of values where status is either "ARAP" or "ACCR".
7.Reset the index of the dataframe and add total records for each of the legal entity, counterparty, and tier by adding new rows to the dataframe and 8.calculating the values for "max(rating by counterparty)", "sum(value where status=ARAP)", and "sum(value where status=ACCR)".



Finally, reset the index of the dataframe and add total records for each of the legal entity, counterparty, and tier by adding new rows to the dataframe and calculating the values for "max(rating by counterparty)", "sum(value where status=ARAP)", and "sum(value where status=ACCR)".

I used the `groupby` function to group the dataframe by 'legal_entity', 'counter_party', and 'tier' columns and used the 'max' and 'sum' aggregation functions to calculate the maximum rating by counterparty and sum of values where status is 'ARAP' and 'ACCR' respectively.

After that, I added three special rows for each legal entity, counterparty & tier with 'Total' values to show the total of each column.

I chose this method because it allows for easy (easier than Apache in my opinion) replication and comprehension of the code, making it suitable for running on a jupyter notebook. 




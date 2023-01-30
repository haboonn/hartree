
# Joining datasets using Pandas and Apache Beam



## Pandas Approach

My thesis for following the course of action I did was to utilize the power of pandas library in python to perform the requested data manipulation task in an efficient and simple way. I followed this course of action because it is an efficient way to perform the necessary transformations on the dataset. Joining the two dataframes on the "counter_party" column ensures that the "tier" column is included in the resulting dataframe. Grouping the dataframe by the "legal_entity", "counterparty", and "tier" columns makes it possible to aggregate the data by those columns. Finally, adding the total records provides a summarized view of the data that makes it easier to understand and analyze. Below is a step by step outline of how I approached this task. 

  *Import the pandas library to use dataframes
  
  *Create two dataframes, dataset1 and dataset2
  *Join the two dataframes on the "counter_party" column
  *Group the resulting dataframe by the "legal_entity", "counterparty", and "tier" columns
  *Use the "max" function on the "rating" column to find the maximum rating by counterparty
  *Use the "sum" function on the "value" column to find the sum of values where status is either "ARAP" or "ACCR".
  *Reset the index of the dataframe and add total records for each of the legal entity, counterparty, and tier by adding new rows to the dataframe and      *calculating the values for "max(rating by counterparty)", "sum(value where status=ARAP)", and "sum(value where status=ACCR)".

Finally, reset the index of the dataframe and add total records for each of the legal entity, counterparty, and tier by adding new rows to the dataframe and calculating the values for "max(rating by counterparty)", "sum(value where status=ARAP)", and "sum(value where status=ACCR)".

I used the `groupby` function to group the dataframe by 'legal_entity', 'counter_party', and 'tier' columns and used the 'max' and 'sum' aggregation functions to calculate the maximum rating by counterparty and sum of values where status is 'ARAP' and 'ACCR' respectively.

After that, I added three special rows for each legal entity, counterparty & tier with 'Total' values to show the total of each column.

I chose this method because it allows for easy (easier than Apache in my opinion) replication and comprehension of the code, making it suitable for running on a jupyter notebook. 



## Apache Beam Approach

The solution I provided to the problem is using Apache Beam library's Python SDK. Apache Beam is a unified programming model for batch and streaming data processing. The solution is divided into the following steps:

*Firstly, I joined the two datasets, ds1 and ds2 on the 'counter_party' column.
*After joining the two datasets, I grouped the data based on the 'legal_entity' and 'counter_party' column
* I calculated the max 'rating' for each group using the beam.CombinePerKey function.
* Calculated the sum of 'value' where the 'status' is 'ARAP' and the sum of 'value' where the 'status' is 'ACCR' using beam.Filter and beam.CombinePerKey function.
* Finally, I formatted the output as required and saved the results.


An issue I ran into with the Apache Beam portion was that I was unable to produce the final results in the Jupyter notebook. As you can see, I am not as proficient in Apache Beam as I am with other python libraries,however I am most definitely open to a challenge when it comes to expanding my skill-set. Apache is a bit more challenging than Pandas for joining datasets due to the size of the datasets, the complexity of the join operations, and the specific use case. For small datasets, Pandas is generally easier to use and provides a more intuitive API for joining data. However, as the size of the datasets grows, the memory limitations of Pandas become more pronounced and Apache becomes a more appropriate choice. Additionally, Apache provides a distributed processing environment, which can make it easier to handle very large datasets. If given the opportunity, I would be eager to use this in a hands-on environment.

The additional information that I would have liked to have is the expected output format for the results.

For  this specific task, having the desired output format along with more detailed instructions,  would have helped me to understand the final outcome of the task and would have made the task more clear.







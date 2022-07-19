# Doing More with Data
## Practice Problems

### Quick problems
Continuing from Monday's session/assuming subway delay data is already loaded to a DataFrame:
* Load `subway_stations.csv` to a DataFrame.
* Check the first 5 rows of `subway_stations`.
* Check `subway_stations` column data types and shape.
* How many unique values are in the `station` column?
* `merge()` the subway station data into `delays_w_reasons`. Make sure that all delay records are kept, even if there is no matching station name in `subway_stations`. The resulting DataFrame should have 16,370 rows.
* Profile the new joined DataFrame. How many delay records are missing station coordinates?

### Pandas workflow practice
#### Getting Data
Select a dataset from [Toronto Open Data](https://open.toronto.ca/catalogue/) or another data portal of your choice, and download it. Some suggested datasets are linked below and additionally available for download in [the course repo /data folder](https://github.com/amfz/dsi-python-workshop/tree/main/data). A good dataset for this exercise will have a mix of data types.

Some sugested datasets:
* [TTC bus delays](https://open.toronto.ca/dataset/ttc-bus-delay-data/): Fewer columns, not well documented, some NaNs. Similar to data we've worked with in class. Recommend choosing a full year of data.
* [Apartment building evaluations](https://open.toronto.ca/dataset/apartment-building-evaluation/): Lots of columns, well-documented, some NaNs.
* [Daily shelter overnight service occupancy and capcity](https://open.toronto.ca/dataset/daily-shelter-overnight-service-occupancy-capacity/): The largest of the datasets suggested. Lots of columns, well-documented, more NaNs.

#### Metadata Review
1. What organization publishes this dataset?
2. How frequently is the dataset updated?
3. What metadata is available (e.g., column names, data types, descriptions)?
4. Is there documentation about who or what produces the data? About who collects it? Through what processes? 
5. Is there documentation about limitations of the data, such as possible sources of error or omission?

#### Getting started
1. Load the data to a single DataFrame.
2. Profile the DataFrame.
   * What are the column names?
   * What are the dtypes when loaded? Do any not make sense?
   * How many NaNs are in each column?
   * What is the shape of the DataFrame?
3. Generate some summary statistics for the data.
   * For numeric columns: What are the max, min, mean, and median?
   * For text columns: What is the most common value? How many unique values are there?
   * Are there any statistics that seem unexpected?
4. Rename one or more columns in the DataFrame.
5. Select a single column and find its unique values.
6. Select a single text/categorical column and find the counts of its values.
7. Convert the data type of at least one of the columns. If all columns are typed correctly, convert one to `str` and back.
8. Write the DataFrame to a different file format than the original.

#### More data wrangling, filtering
1. Create a column derived from an existing one. Some possibilities:
   * Bin a continuous variable
   * Extract a date or time part (e.g. hour, month, day of week)
   * Assign a value based on the value in another column (e.g. TTC line number based on line values in the subway delay data)
   * Replace text in a column (e.g. replacing occurrences of "Street" with "St.")
2. Remove one or more columns from the dataset.
3. Extract a subset of columns and rows to a new DataFrame
   * with the `.query()` method and column selecting `[[colnames]]`
   * with `.loc[]`
4. Investigate null values
   * Create and describe a DataFrame containing records with NaNs in any column
   * Create and describe a DataFrame containing records with NaNs in a subset of columns
   * If it makes sense to drop records with NaNs in certain columns from the original DataFrame, do so.

#### Grouping and aggregating
TBA

# Pandas

## Reading

### [Pandas in 10](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html)

- customary import:

  ```python
  import numpy as np
  import pandas as pd
  ```

- Object creation scenarios:
  - Creating a Series by passing a list of values, letting pandas create a default integer index
  - Creating a DataFrame by passing a NumPy array, with a datetime index using date_range() and labeled columns
  - Creating a DataFrame by passing a dictionary of objects that can be converted into a series-like structure

- Viewing data:
  - Use DataFrame.head() and DataFrame.tail() to view the top and bottom rows of the frame respectively
  - DataFrame.to_numpy() gives a NumPy representation of the underlying data
    - Note that this can be an expensive operation when your DataFrame has columns with different data types, which comes down to a fundamental difference between pandas and NumPy:
      - NumPy arrays have one dtype for the entire array, while pandas DataFrames have one dtype per column
  - When you call DataFrame.to_numpy(), pandas will find the NumPy dtype that can hold all of the dtypes in the DataFrame.
    - This may end up being object, which requires casting every value to a Python object.

- Selection:
  - While standard Python / NumPy expressions for selecting and setting are intuitive and come in handy for interactive work, for production code, we recommend the optimized pandas data access methods, DataFrame.at(), DataFrame.iat(), DataFrame.loc() and DataFrame.iloc().
  - Getting:
  - Selection by label:
  - Selection by position:
  - Boolean indexing:
  - Setting:

- Missing data:
  - pandas primarily uses the value np.nan to represent missing data. It is by default not included in computations.
  - Reindexing allows you to change/add/delete the index on a specified axis. This returns a copy of the data

- Operations:
  - Stats:
    - operations in general exclude missing data
    - Operating with objects that have different dimensionality and need alignment. In addition, pandas automatically broadcasts along the specified dimension
  - Apply: DataFrame.apply() applies a user defined function to the data
  - Histogramming
  - String Methods:
    - Series is equipped with a set of string processing methods in the str attribute that make it easy to operate on each element of the array, as in the code snippet below.
    - Note that pattern-matching in str generally uses regular expressions by default (and in some cases always uses them).

- Merge:
  - Concat:
    - pandas provides various facilities for easily combining together Series and DataFrame objects with various kinds of set logic for the indexes and relational algebra functionality in the case of join / merge-type operations.
    - Adding a column to a DataFrame is relatively fast. However, adding a row requires a copy, and may be expensive. We recommend passing a pre-built list of records to the DataFrame constructor instead of building a DataFrame by iteratively appending records to it.
  - Join:
    - merge() enables SQL style join types along specific columns.

- Grouping
  - By “group by” we are referring to a process involving one or more of the following steps:
    - Splitting the data into groups based on some criteria
    - Applying a function to each group independently
    - Combining the results into a data structure

- Reshaping
  - Stack
    - The stack() method “compresses” a level in the DataFrame’s columns
    - With a “stacked” DataFrame or Series (having a MultiIndex as the index), the inverse operation of stack() is unstack(), which by default unstacks the last level
  - Pivot tables
    - pivot_table() pivots a DataFrame specifying the values, index and columns

- Time series
  - pandas has simple, powerful, and efficient functionality for performing resampling operations during frequency conversion (e.g., converting secondly data into 5-minutely data).
    - This is extremely common in, but not limited to, financial applications.
  - Converting between period and timestamp enables some convenient arithmetic functions to be used.

- Categoricals
  - pandas can include categorical data in a DataFrame

- Plotting

- Importing and exporting data
  - CSV
    - Writing to a csv file: using DataFrame.to_csv()
    - Reading from a csv file: using read_csv()
  - HDF5
    - Writing to a HDF5 Store using DataFrame.to_hdf()
    - Reading from a HDF5 Store using read_hdf()
  - Excel
    - Writing to an excel file using DataFrame.to_excel()
    - Reading from an excel file using read_excel()

- Gotchas
  - If you are attempting to perform a boolean operation on a Series or DataFrame you might see an exception

## Additional Resources

### [Pandas - Getting Started](https://pandas.pydata.org/pandas-docs/stable/getting_started/intro_tutorials/index.html)

### [Real Python - Pandas Tutorials](https://realpython.com/learning-paths/pandas-data-science/)

## Videos

### [What is Pandas](https://www.youtube.com/watch?v=dcqPhpY7tWk&t=391s)

### [Pandas Tutorials](https://www.youtube.com/playlist?list=PL-osiE80TeTsWmV9i9c58mdDCSskIFdDS) - alternate option

### More Additional Resources

### [Master Pandas](https://towardsdatascience.com/be-a-more-efficient-data-scientist-today-master-pandas-with-this-guide-ea362d27386)

---

## Reading Questions

- Explain the purpose and basic functionality of the Pandas library. What are some common operations that can be performed on data using Pandas, and how do they contribute to data analysis and manipulation?
  - Pandas is an open-source python library that is used for data manipulation and analysis. It provides many functions and methods to speed up the data analysis process. Pandas is built on top of the NumPy package, hence it takes a lot of basic inspiration from it. The two primary data structures are Series which is 1 dimensional and DataFrame which is 2 dimensional.
  - Reading & writing data, Data cleaning, Data filtering and selction, Data aggregation, Data visualization

- What are the primary data structures in Pandas, and how do they differ in terms of use cases?
  - Series, and DataFrame
  - The primary difference between Series and DataFrame is that a Series represents a single column of data, while a DataFrame can contain multiple columns of data.

- Describe the process of loading a dataset into a Pandas DataFrame. What are some common file formats that can be used, and which Pandas functions are utilized to read these formats?
  - Import the pandas lib, specify the file path, read the file, explore the data
  - CSV, Excel, JSON, SQL, HDF5

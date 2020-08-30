# Read:12 Summary
## Pandas 
* `pandas` is a Python package providing fast, flexible, and expressive data structures designed to make working with “relational” or “labeled” data both easy
and intuitive. It aims to be the fundamental high-level building block for doing practical, real world data analysis in Python. Additionally, it has the broader
goal of becoming ***the most powerful and flexible open source data analysis / manipulation tool available in any language***. It is already well on its
way toward this goal.
* `Pandas` is a game-changer for data science and analytics, particularly if you came to Python because you were searching for something more powerful 
than Excel and VBA. Pandas uses fast, flexible, and expressive data structures designed to make working with relational or labeled data
both easy and intuitive.


***pandas is well suited for many different kinds of data:***


  * Tabular data with heterogeneously-typed columns, as in an SQL table or Excel spreadsheet


  * Ordered and unordered (not necessarily fixed-frequency) time series data.


  * Arbitrary matrix data (homogeneously typed or heterogeneous) with row and column labels


  * Any other form of observational / statistical data sets. The data actually need not be labeled at all to be placed into a pandas data structure
  
  
  
***The two primary data structures of pandas :***


  * Series (1-dimensional) ( 1D labeled homogeneously-typed array )

 
  * DataFrame (2-dimensional) (  General 2D labeled, size-mutable tabular structure with potentially heterogeneously-typed column )  
  --------------------------------------------------------------------------------------------------------------------------------------------------
  
* `Pandas` handle the vast majority of typical use cases in finance, statistics, social science, and many areas of engineering
* `pandas` is built on top of NumPy and is intended to integrate well within a scientific computing environment with many other 3rd party libraries.


***Here are just a few of the things that pandas does well:***


  * Easy handling of missing data (represented as NaN) in floating point as well as non-floating point data


  * Size mutability: columns can be inserted and deleted from DataFrame and higher dimensional objects


  * Automatic and explicit data alignment: objects can be explicitly aligned to a set of labels, or the user can simply ignore the labels and let Series, 
  DataFrame, etc. automatically align the data for you in computations


  * Powerful, flexible group by functionality to perform split-apply-combine operations on data sets, for both aggregating and transforming data


  * Make it easy to convert ragged, differently-indexed data in other Python and NumPy data structures into DataFrame objects


  * Intelligent label-based slicing, fancy indexing, and subsetting of large data sets


  * Intuitive merging and joining data sets


  * Hierarchical labeling of axes (possible to have multiple labels per tick)


  * Robust IO tools for loading data from flat files (CSV and delimited), Excel files, databases, and saving / loading data from the ultrafast HDF5 format


  * Time series-specific functionality: date range generation and frequency conversion, moving window statistics, date shifting and lagging.
----------------------------------------------------------------------------------------------------------------------------------------------

* `pandas` is a dependency of statsmodels, making it an important part of the statistical computing ecosystem in Python.

* `pandas` has been used extensively in production in financial applications.

* DataFrame is a container for Series, and Series is a container for scalars. We would like to be able to insert and remove objects from 
these containers in a dictionary-like fashion.
* `All pandas data structures` are value-mutable (the values they contain can be altered) but not always size-mutable. The length of a Series cannot be 
changed, but, for example, columns can be inserted into a DataFrame


* ***To start using pandas :*** `import pandas as pd`


* `Each column in a DataFrame is a Series`
------------------------------------------------------------------------------------------------------------------------------------------------------

## The most elementary functions of pandas

* Reading data : `data = pd.read_csv('my_file.csv')`
* Writing data : `data.to_csv('my_new_file.csv', index=None)`
* Checking the data : `data.shape` OR `data.describe()`
* Seeing the data : `data.head(3)` OR `data.loc[8]` OR `data.loc[8, 'column_1']` OR `data.loc[range(4,6)]`
## The basic functions of pandas

* Logical operations :
  * `data[data['column_1']=='french']`
  * `data[(data['column_1']=='french') & (data['year_born']==1990)]`
  * `data[(data['column_1']=='french') & (data['year_born']==1990) & ~(data['city']=='London')]`
  * `data[data['column_1'].isin(['french', 'english'])]`
* Basic plotting

  * `data['column_numerical'].plot()`
  * `data['column_numerical'].hist()`
  * `%matplotlib inline/`
  
* Updating the data
  * `data.loc[8, 'column_1'] = 'english'`
  * `data.loc[data['column_1']=='french', 'column_1'] = 'French'`
### Medium level functions
* Counting occurrences
  * `data['column_1'].value_counts()`
* Operations on full rows, columns, or all data
  * `data['column_1'].map(len)`
  * `data['column_1'].map(len).map(lambda x: x/100).plot()`
  * `data.apply(sum)`
* Correlation and scatter matrices
  * `data.corr()`
  * `data.corr().applymap(lambda x: int(x*100)/100)`
  * `pd.plotting.scatter_matrix(data, figsize=(12,8))`
### Advanced operations in pandas

* The SQL join
  * `data.merge(other_data, on=['column_1', 'column_2', 'column_3'])`
* Grouping
  * `data.groupby('column_1')['column_2'].apply(sum).reset_index()`
* Iterating over rows
  * `dictionary = {}`
  * `for i,row in data.iterrows():`
  * ` dictionary[row['column_1']] = row['column_2']`
### Conclusion 
* Panda is simple to use, hiding all the complex and abstract computations behind
* Panda is (generally) intuitive
* Panda is fast, if not the fastest data analysis package (it highly optimized in C)
* It is THE tool that helps a data scientist to quickly read and understand data and be more efficient at his role.


























































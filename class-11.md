# Read:11 Summary

## Data Science
* It is a set of disciplines and practices that handle data in a scientific manner. The foundations
of data science are mostly Mathematics and Statistics, sometimes Software Engineering would play a role as well
* there are some definitions for the data science :
  * “Data science is an interdisciplinary field about processes and systems to extract knowledge or insights from data in various forms, either structured or 
  unstructured, which is a continuation of some of the data analysis fields such as statistics, data mining, and predictive analytics, similar to Knowledge 
  Discovery in Databases.” – Wikipedia


  * “The science of dealing with data, once they have been established, while the relation of the data to what they represent 
  is delegated to other fields and sciences.” – Peter Naur


  * “By ‘Data Science’ we mean almost everything that has something to do with data: Collecting, analyzing, 
  modeling…” – The Journal of Data Science

* Usually, it includes but not limited to these steps:
  * Data acquisition : To play with data, you need to have data first.
    * The data could be in the form of .CSV files. Excel file (.XLSX) is a typical form, or it could be available by API calls, or someone has done
    the dirty work already and they are all in DWH(Data WareHouse) or Data Lake.


  * Data cleaning & wrangling : In the actual working environment, data is rarely ready to be used right away.
    * Data could be in the nested structure for storage saving purpose (e.g. Bigquery and NoSQL), could be normalized (like general databases). The data 
    need to be flattened before usage.

  * Data Engineering : It is a extremely vital part as all kinds of data science tricks depends on it.
    * If there is no good data to use, NONE of the data science gimmicks could work.
    * Well engineered data should be clean, fast and cheap (in terms of computational resources, hence money as well) for robust
    consumption right away.


  * Utilization of data : This is the sexy part that people couldn’t stop talking about.
    * From traditional consumption like building an application, doing ad hoc analysis, dashboarding and the recent fancy thing such as 
    Machine Learning, this is the step people care so much.
    
 ---------------------------------------------------------------------------------------------------------------------------------------------

## JupyterLab
* JupyterLab is a next-generation web-based user interface for Project Jupyter.
* JupyterLab enables you to work with documents and activities such as Jupyter notebooks, text editors, terminals, and custom
components in a flexible, integrated, and extensible manner
* You can arrange multiple documents and activities side by side in the work area using tabs and splitters. Documents and activities
integrate with each other, enabling new workflows for interactive computing
* JupyterLab also offers a unified model for viewing and handling data formats. JupyterLab understands many file formats (images, CSV, JSON, Markdown, PDF, Vega, Vega-Lite, etc.)
and can also display rich kernel output in these formats
--------------------------------------------------------------------------------------------------------------------------------------------------
## NumPy Tutorial: Data Analysis with Python

* `NumPy` : which stands for Numerical Python, is a library consisting of multidimensional array objects and a collection of routines for processing those arrays.
Using NumPy, mathematical and logical operations on arrays can be performed.
* `NumPy` :  is a commonly used Python data analysis package. By using NumPy, you can speed up your workflow, and interface with other packages in the Python
ecosystem, like scikit-learn, that use NumPy under the hood. NumPy was originally developed in the mid 2000s, and arose from an even older 
package called Numeric. This longevity means that almost every data analysis or machine learning package for Python leverages NumPy in some way.

* Before using NumPy, we’ll first try to work with the data using Python and the csv package :
  * Import the `csv` library.
  * Open the .csv file.

  * With the file open, create a new csv.reader object.

  * etc...

* With NumPy, we can work with multidimensional arrays.we’ll focus on 2-dimensional arrays. A 2-dimensional array is also known as a matrix or ( list of lists). A matrix 
has rows and columns.By specifying a row number and a column number, we’re able to extract an element from a matrix.
* the core of NumPy is written in a programming language called C, which stores data differently than the Python data types. NumPy data types map between Python and C, allowing
us to use NumPy arrays without any conversion hitches.
* NumPy has several different data types, the important ones are :
  * `float` — numeric floating point data.

  * `int` — integer data.
  * `string` — character data.
  * `object` — Python objects

* NumPy makes it simple to perform mathematical operations on arrays. This is one of the primary advantages of NumPy, and makes it
quite easy to do computations.

* NumPy makes it possible to test to see if rows match certain values using mathematical comparison operations like `<, >, >=, <=, and ==`
* With NumPy, it’s very common to combine multiple arrays into a single unified array


***you can see the NumPy sheet cheat in this link : https://s3.amazonaws.com/dq-blog-files/numpy-cheat-sheet.pdf***



----------------------------------------------------------------------------------------------------------------------



















  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  




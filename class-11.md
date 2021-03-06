# Explore the Tech!

## 1. _Jupyter_ Lab:
JupyterLab enables you to work with documents and activities such as Jupyter notebooks, text editors, terminals, and custom components in a flexible, integrated, and extensible manner.

You can arrange multiple documents and activities side by side in the work area using tabs and splitters.
Documents and activities integrate with each other, enabling new workflows for interactive computing, for example:

* Code Consoles provide transient scratchpads for running code interactively, with full support for rich output. A code console can be linked to a notebook kernel as a computation log from the notebook, for example.
* Kernel-backed documents enable code in any text file (Markdown, Python, R, LaTeX, etc.) to be run interactively in any Jupyter kernel.
* Notebook cell outputs can be mirrored into their own tab, side by side with the notebook, enabling simple dashboards with interactive controls backed by a kernel.
* Multiple views of documents with different editors or viewers enable live editing of documents reflected in other viewers. For example, it is easy to have live preview of Markdown, Delimiter-separated Values, or Vega/Vega-Lite documents.


## 2. Numpy:
NumPy is a commonly used Python data analysis package. By using NumPy, you can speed up your workflow, and interface with other packages in the Python ecosystem, like scikit-learn, that use NumPy under the hood. NumPy was originally developed in the mid 2000s, and arose from an even older package called Numeric. 
This longevity means that almost every data analysis or machine learning package for Python leverages NumPy in some way.

##### Creating A NumPy Array
We can create a NumPy array using the numpy.array function. 
If we pass in a list of lists, it will automatically create a NumPy array with the same number of rows and columns. Because we want all of the elements in the array to be float elements for easy computation, we’ll leave off the header row, which contains strings. One of the limitations of NumPy is that all the elements in an array have to be of the same type, so if we include the header row, all the elements in the array will be read in as strings. 
Because we want to be able to do computations like find the average quality of the wines, we need the elements to all be floats.

Steps: 
* Import the numpy package.
* Pass the list of lists wines into the array function, which converts it into a NumPy array.
* Exclude the header row with list slicing.
* Specify the keyword argument dtype to make sure each element is converted to a float.

##### Indexing NumPy Arrays
We now know how to create arrays, but unless we can retrieve results from them, there isn’t a lot we can do with NumPy. 
We can use array indexing to select individual elements, groups of elements, or entire rows and columns. One important thing to keep in mind is that just like Python lists, `NumPy` is zero-indexed, meaning that the index of the first row is `0`, 
and the index of the first column is `0`. If we want to work with the fourth row, we’d use index `3`, if we want to work with the second row, we’d use index `1`, and so on.

##### Slicing NumPy Arrays
If we want to select the first three items from the fourth column, we can do it using a colon `(:)`.
A colon indicates that we want to select all the elements from the starting index up to but not including the ending index. This is also known as a `slice`.

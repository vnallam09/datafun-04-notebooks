# RUN_ALL.md

> Running All the Examples

## Before Running

The examples include both Python scripts (.py) and Jupyter Notebooks (.ipynb), 
so to execute all of the examples, you'll need to be able to:

1. Start an interactive Python session
1. Read and execute a Python script (.py)
1. Read and execute a Jupyter notebook (.ipynb)

To read and execute Jupyter notebooks, you should be able to:

1. Open a notebook
1. Run the notebook
1. Run a cell in the notebook (Shift Enter or Shift Return)
1. Recognize and read Markdown cells
1. Recognize and read Python cells

## Set Your Python Interpreter 

You may have more than one Python environment on your machine, 
e.g., one for work projects and one for school projects.
In this class, we use Python version 3.11+.

1. From VS Code Menu / View / Command Palette /
1. Type Python: Select Interpreter
1. Choose the Python 3.11 option (it shows the locations of all options) associated with your project.

## VS Code and Jupyter  

We may execute scripts (.py) and notebooks (.ipynb) from the command line,
but we want to run them VS Code (or other editor) to get the 
benefits of autocompletion, formatting, git integration, and more. 

When opening these new external files in your existing VS Code Python environment, 
you may find that it reverts back to a standard Python interpreter (maybe 3.9 when we're using 3.11). 
Use the steps above to set your Python interpreter, and restart VS Code.

You can also use the kernel selection in the upper right that comes with the VS Code Jupyter extension. 
More information is available here [Jupyter Notebooks in VS Code](https://code.visualstudio.com/docs/datascience/jupyter-notebooks).


## Install Additional Modules

Python comes with a large Python Standard Library, but we often 
want additional classes, modules, and packages for even
more functionality. 

For example, when trying out new code, you may get a Module Not Found Error, e.g.,

`ModuleNotFoundError: No module named 'matplotlib'`

That means the Python interpreter can't find that module in your active environment. 
You'll need to download and install it using a package manager like pip or conda.  

## Install Additional Modules

To work with all the textbook examples, you'll need the following installed in your active environment.

- beautifulsoup4 - data from web pages
- dweepy - device feeds
- geopy - geographic information
- imageio - work with images
- jupyterlab - very popular web-based analytics environment
- matplotlib - custom charts
- nltk - natural language toolkit
- numpy - 1D Arrays
- pandas - 2D panel / sheet data
- prospector - static code analysis
- pymongo - work with noSQL datastore MongoDB and Atlas
- pyspark - work with Apache Spark
- scikit-learn - machine learning
- scipy - statistics and scientific computing
- seaborn - quick charts
- spacy - natural language processing
- tensorflow - machine learning
- textatistic - readability metrics
- textblob - text processing
- wordcloud - visualize frequency of text

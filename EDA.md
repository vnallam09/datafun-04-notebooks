## Exploratory Data Analysis

Objective: Implement Jupyter Notebook to perform exploratory data analysis (EDA) using pandas and other tools. 
We will use the Seaborn library to load the Iris dataset. 
Review the dataset here: iris.csv or see the local copy provided iris.csv.

## Step 1. Initial Title, Header, and Imports

1. Create a single Markdown title. 
2. Create a Markdown header with author name, purpose, and date at the top.
3. Create a numbered section for Imports (using a Markdown cell).
4. Create a Python cell for all the import statements needed for this notebook.

## Step 2. Load Data
The Iris dataset is a well-known dataset in data science and machine learning, often used for various classification tasks and basic data exploration. 
Load the data into a pandas DataFrame. 
For this step, it's common to use pandas methods such as pd.read_csv() or pd.read_excel() as appropriate. 
We'll use sns.load_dataset() function and pass in the 'iris' (the name without .csv) to populate our DataFrame.

Jupyter Notebook / Python cell example:

```python
# Load the Iris dataset into DataFrame
df: pd.DataFrame = sns.load_dataset('iris')

# Inspect first rows of the DataFrame
print(df.head())
```


## Step 3. Initial Data Inspection
Display the first 10 rows of the DataFrame, check the shape, and display the data types of each column using df.head(10), df.shape, and df.dtypes.

Jupyter Notebook / Python cell example:
```python
print(df.head(10))
print(df.shape)
print(df.dtypes)
```

## Step 4. Initial Descriptive Statistics
Use the DataFrame describe() method to display summary statistics for each column.

Jupyter Notebook / Python cell example:
```python
print(df.describe())
```

## Step 5. Initial Data Distribution for Numerical Columns
Choose a numerical column and use df['column_name'].hist() to plot a histogram for that specific column. To show all the histograms for all numerical columns, use df.hist().

Jupyter Notebook / Python cell example:
```python
# Inspect histogram by numerical column
df['sepal_length'].hist()

# Inspect histograms for all numerical columns
df.hist()

# Show all plots
plt.show()
```
Afterwards, use a Markdown cell to document your observations.

## Step 5. Initial Data Distribution for Categorical Columns
Choose a categorical column and use df['column_name'].value_counts() to display the count of each category. 
Use a loop to show the value counts for all categorical columns.

Jupyter Notebook / Python cell example:
```python
# Inspect value counts by categorical column
# You must know the name of the data columns available. 
df['species'].value_counts()

# Inspect value counts for all categorical columns
for col in df.select_dtypes(include=['object', 'category']).columns:
    # Display count plot
    sns.countplot(x=col, data=df)
    plt.title(f'Distribution of {col}')
    plt.show()

# Show all plots
plt.show()
```

Afterwards, use a Markdown cell to document your observations.

## Step 6. Initial Data Transformation and Feature Engineering
Use pandas and other tools to perform transformations as needed. Transformation may include renaming columns, adding new columns, or transforming existing data for more in-depth analysis.

Jupyter Notebook / Python cell example:
```python
# Renaming a column
df.rename(columns={'sepal_length': 'Sepal Length'}, inplace=True)

# Adding a new column
df['Sepal Area'] = df['Sepal Length'] * df['sepal_width']
```

## Step 7. Initial Visualizations
Create a variety of chart types using seaborn and matplotlib to showcase different aspects of the data. There is a guided example in the resources section at the end of this document.

Jupyter Notebook / Python cell example:
```python
sns.pairplot(df, hue='species')
plt.show()
```
Important: After each visualization, use Markdown cells to document your observations and insights.

## Step 8. Initial Insights
Use your chart headings and annotations to provide your insights. 
At the end add a section that summarizes your initial insights based on the facts discovered during your initial exploratory data analysis. 

## Step 9. Annotate Your Notebook for Storytelling and Presentation
Present your notebook with an opening that introduces yourself and your topic. Use Markdown section headings to introduce each step. Interpret the visualizations and statistics to narrate a clear and compelling data story. Present your findings in a logical and engaging manner.

## Checklist

- [ ] Notebook has exactly one Markdown title (with a single hash).
- [ ] Notebook has useful Markdown header cell with author and purpose, and optionally, the date.
- [ ] Notebook uses numbered second level Markdown headings for organization. 
- [ ] Notebook has numbered sections with useful content for:
  - [ ] 1. Imports
  - [ ] 2. Load Data
  - [ ] 3. Initial Data Inspection
  - [ ] 4. Initial Descriptive Statistics
  - [ ] 5. Initial Data Distribution for Numerical Columns
  - [ ] 6. Initial Data Transformation and Feature Engineering
  - [ ] 7. Initial Visualizations
  - [ ] 7. Initial Insights
- [ ] Notebook includes commentary as we go that tells a unique data story. 
- [ ] Notebook includes unique insights into the dataset. 
- [ ] Code and visuals are working, notebook is fully executed and on display in GitHub. 

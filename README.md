# Introduction to Jupyter Notebooks in VS Code

Jupyter Notebooks are a popular way to create and share documents for data analytics. 
They are interactive, easy to share, and support a wide variety of data science tools.

When employers ask for years of experience with a language, it's not the syntax - that can be learned in a few days. 
It's the experience with the tools, libraries, and frameworks that takes time.

IMPORTANT: To run Jupyter within VS Code, use the Jupyter extension. Go to the Extensions pane on the left sidebar (the icon looks like four squares), searching for "Jupyter," and installing the "Jupyter" extension provided by Microsoft.

## Project Requirements

- VS Code
- Git
- Python 

## Professional Python Workflow

See [pro-analytics-01](https://github.com/denisecase/pro-analytics-01/)

## Commands to Manage Virtual Environment

For Windows PowerShell (change if using Mac/Linux).
Verify that all required packages are included in requirements.txt (and have NOT been commented out).

```powershell
py -m venv .venv
.\.venv\Scripts\activate
py -m pip install --upgrade pip setuptools wheel
py -m pip install --upgrade -r requirements.txt
```

## Commands to Run Python Scripts

Remember to activate your .venv (and install packages if they haven't been installed yet) before running files.

```shell
py demo-script.py
```

## Commands to Git add-commit-push

```shell
git add .
git commit -m "custom message"
git push -u origin main
```

## Task 1: Use and Explore the Demo Project / Repository / Notebook

### Step 1: Copy and Clone the Example Repository
1. Click "Use this template" on this example repository (if it's not a template, click "Fork" instead).
2. Clone the repository to your machine:
   git clone example-repo-url
3. Open your new cloned repository in VS Code.

### Step 2: Set Up and Run the Demo Notebook
Next, create and activate a virtual environment for this project. 
Also install additional dependencies required for this project.
See [requirements.txt](requirements.txt) for detailed instructions. 

A. Create .venv
B. Activate .venv
C. Install dependencies into .venv
D. Select VS Code interpreter to use .venv

### Step 3: Open Notebook, Create/Select Kernel
1. Open the provided Jupyter Notebook (`demo-notebook.ipynb`):
2. Create and select the notebook kernel. See [requirements.txt](requirements.txt) **Step E** for detailed instructions. 

### Step 4: Explore the Notebook Cells and Code
Open the Notebook and click Run all to execute it.
- Explore how notebooks have cells. 
- Our notebook cells are either Markdown or Python. 
- Try to add new cells.
- Try to change the type of a cell.
- Try some Markdown in a Markdown cell.
- Try some Python in a Python cell. 
- Review the code and see how it works. 

---

## Troubleshooting and Tips
- See [TROUBLESHOOTING.md](docs/TROUBLESHOOTING.md)

## Additional Resources 
- See [RESOURCES.md](docs/RESOURCES.md)

## Reference Projects

Custom implementation of the example project at 
[datafun-04-notebooks](https://github.com/denisecase/datafun-04-notebooks/)

- [datafun-03-analytics](https://github.com/denisecase/datafun-03-analytics/)
- [datafun-02-project-setup](https://github.com/denisecase/datafun-02-project-setup/)
- [datafun-01-utils](https://github.com/denisecase/datafun-01-utils/)
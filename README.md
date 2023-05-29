# Introduction to Jupyter Notebooks in VS Code

- [GitHub Repository](https://github.com/denisecase/datafun-04-notebooks/)

Jupyter Notebooks are a popular way to create and share documents for data analytics. They are interactive, easy to share, and support a wide variety of data science tools.

## Step 1: Open The Project Folder

Open VS Code and clone your `datafun-04-notebooks` repository to your machine.

## Step 2: Update Default Python

Open a terminal in VS Code. Use the menu View / Terminal. 
In Windows, use PowerShell, in Mac, use bash.
Verify you've added some essential packages to your default Python environment.

```shell
python -m pip install --upgrade pip ipykernel jupyterlab
python -m pip install --upgrade black ruff
```

Note: If `py` or `python3` works on your machine, use that instead of `python` in the commands.

-----

## Step 3: Add Common Files

When starting a new project, there are some common files you should add to the project folder.

### Add .gitignore

- The .gitignore file tells Git files to ignore when committing changes.
- Review the [gitignore](gitignore) file, you can use it without modification.

### Modify README.md

- Learn to edit and customize README.md files, which provide a quick overview of the project and instructions for running it. 

### Scan requirements.txt

- The requirements.txt file lists the packages used in the project.
- You may not use all them and may want to add others. Modify this list as you like. 

🚀 Rocket Tip: When employers ask for years of experience with a language, it's not the syntax - that's learned in a few days. It's the experience with the tools, libraries, and frameworks that takes time.

-----

## Step 4: Set up a Virtual Enviroment

Next, we'll create and activate a virtual environment specifically for this project. We'll also install additional packages required for this project.

### Create a Virtual Environment

1. Open the terminal in VS Code. (View / Terminal)
2. Run the following command to **create** a virtual environment for this project.

```shell
python -m venv .venv
```

Verify that a new `.venv` folder was created. It may take a while for the command to complete.

🚀 Rocket Tip: When VS Code Python Extension offers to select the Environment, say Yes.

### Activate the Virtual Environment

Wait for the creation to finish, then **activate** the virtual environment:

- For PowerShell: `.venv\Scripts\Activate`
- For macOS/Linux:  `source .venv/bin/`

🚀 Rocket Tip: Notice the terminal changes to reflect the active virtual environment.

### Install Dependencies to the Active Virtual Environment

Install additional project dependencies into the active virtual environment.
The packages ipykernel and jupyterlab are required to run a notebook.
The packages pandas, matplotlib, and seaborn are used to work with data and charts.

```shell
python -m pip install --upgrade pip ipykernel jupyterlab
python -m pip install --upgrade pandas matplotlib seaborn
python -m pip install --upgrade voila
```

Alternatively, you can install all the packages listed in the requirements.txt file.

```shell
python -m pip install --upgrade -r requirements.txt
```

Note: The `--upgrade` parameter gets the lastest version of each package.

-----

## Step 5: Working with Notebooks

In the active virtual environment, create a Python kernel to run our notebooks. 

```shell
python -m ipykernel install --user --name .venv --display-name "Python (.venv)"
```

### Execute an existing notebook


### Create a new notebook

In VS Code, from the menu, select View / Command Palette.
Type `notebook` and select `Jupyter: Create New Blank Notebook`.
This will create a new notebook in the project folder.
Save the notebook with a name like `yourname-notebook.ipynb`.




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

When employers ask for years of experience with a language, it's not the syntax - that's learned in a few days. It's the experience with the tools, libraries, and frameworks that takes time.

-----

## Step 4: Set up a Virtual Environment

Next, we'll create and activate a virtual environment specifically for this project. We'll also install additional packages required for this project.

### Create a Virtual Environment

1. Open the terminal in VS Code. (View / Terminal)
2. Run the following command to **create** a virtual environment for this project.

```shell
python -m venv .venv
```

Verify that a new `.venv` folder was created. It may take a while for the command to complete.

When VS Code Python Extension offers to select the Environment, say Yes.

### Activate the Virtual Environment

Wait for the creation to finish, then **activate** the virtual environment:

- For PowerShell: `.venv\Scripts\Activate`
- For macOS/Linux:  `source .venv/bin/`

Notice the terminal changes to reflect the active virtual environment.

### Install Dependencies to the Active Virtual Environment

Install additional project dependencies into the active virtual environment.
The packages ipykernel and jupyterlab are required to run a notebook.
The packages pandas, matplotlib, and seaborn are used to work with data and charts.

```shell
python -m pip install --upgrade pip ipykernel jupyterlab
python -m pip install --upgrade pandas matplotlib seaborn
```

Alternatively, you can install all the packages listed in the requirements.txt file.

```shell
python -m pip install -r requirements.txt
```

Note: The `--upgrade` parameter gets the latest version of each package.

-----

## Step 5: Create a Notebook and Set the Kernel

In the active virtual environment, create a Python kernel to run our notebooks. 

```shell
python -m ipykernel install --user --name .venv --display-name "Python (.venv)"
```

### 5.1 Create a new notebook

In VS Code, from the menu, select View / Command Palette.

Type `notebook` and select `Jupyter: Create New Blank Notebook`.
This will create a new notebook in the project folder.

Save the notebook with a name like `yourname-notebook.ipynb`.


### 5.2 Select the virtual environment for the notebook kernel

In VS Code, from the menu, select View > Command Palette.

Type kernel and select Notebook: Select Notebook Kernel.
Choose the kernel named "Python (.venv)" from the list.

This ensures your notebook uses the packages installed in your virtual environment.

-----

## Troubleshooting

If you've created the .venv virtual environment,  installed the necessary packages, 
and selected a Kernel for your Jupyter Notebook, it should run - 
even if the code shows a missing package error. See the image below.

![Check Kernel and .venv. VS Code may show an issue, but may still work](images/VSCode-SelectKernel-AndInstallPkgs-Then-It-Should-Run-Even-With-NotFound-Issue.PNG)

Why Your Notebook May Still Not See a Package

If the Jupyter notebook kernel is not set to the same environment where you installed the package, the package won't be found. This can happen if:

- The terminal in VS Code is pointed to one virtual environment, but the Jupyter kernel is using another. This can occur if you have multiple virtual environments and accidentally select the wrong one for your Jupyter notebook.
- Even if you try to manually point the kernel to the right environment, there might be path conflicts or misconfigurations that prevent the notebook from recognizing the installed packages.

### Recommendations

Recommendation 1: Keep Virtual Environment and Kernel Aligned

The environment where the Jupyter server runs (where a !pip install in your notebook would install packages) might differ from the environment where the notebook kernel runs. 
This can lead to scenarios where a package appears installed in the terminal but isn't accessible within the notebook.
Whenever you create a new virtual environment and want to use it with Jupyter notebooks, you need to install ipykernel and your necessary packages in that environment.

Recommendation 2: Use Magic Commands (Jupyter commands use %)

Once your project virtual environment and kernel are aligned, if you still have issues, then use magic commands. 
Magic commands are interpreted by the IPython kernel and provide a way to interact with the underlying Python environment directly. 
Using %pip install ensures that the package is installed in the same environment as the notebook kernel. 
To use a magic command, in your Jupyter Notebook, add a Python cell with the following command:

```python
%pip install scikit-learn
```

Note that we don't use the leading py -m that we do when running Python utility commands (pip, venv, etc.) in the terminal. 

Virtual environments are recommended to ensure isolation and reproducibility of your project's dependencies. 
If you encounter issues with virtual environments and need to install packages directly within a notebook, using magic commands is a reliable alternative.

Avoid: Shell Commands for Installs (Shell Commands use !)

Don't use !pip install (with an exclamation instead of percent). 
This is a shell command, which means it runs in the shell environment of the system where the Jupyter server is running. 
While it can work, it might not install the package in the same environment that the notebook kernel is using, especially in environments with multiple Python installations or virtual environments.

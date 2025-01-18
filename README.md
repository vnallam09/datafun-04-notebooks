# Introduction to Jupyter Notebooks in VS Code

Jupyter Notebooks are a popular way to create and share documents for data analytics. 
They are interactive, easy to share, and support a wide variety of data science tools.

When employers ask for years of experience with a language, it's not the syntax - that can be learned in a few days. 
It's the experience with the tools, libraries, and frameworks that takes time.

---

## Task 1: Use and Explore the Demo Project / Repository / Notebook

### Step 1.1: Copy and Clone the Example Repository
1. Click "Use this template" on this example repository (if it's not a template, click "Fork" instead).
2. Clone the repository to your machine:
   git clone example-repo-url
3. Open your new cloned repository in VS Code.

### Step 1.2: Set Up and Run the Demo Notebook
Next, create and activate a virtual environment for this project. 
Also install additional dependencies required for this project.
See [requirements.txt](requirements.txt) for detailed instructions. 

A. Create .venv
B. Activate .venv
C. Install dependencies into .venv
D. Select VS Code interpreter to use .venv

### Step 1.3: Open Notebook, Create/Select Kernel
1. Open the provided Jupyter Notebook (`demo-notebook.ipynb`):
2. Create and select the notebook kernel. See [requirements.txt](requirements.txt) **Step E** for detailed instructions. 

### Step 1.4: Explore the Notebook Cells and Code
Open the Notebook and click Run all to execute it.
- Explore how notebooks have cells. 
- Our notebook cells are either Markdown or Python. 
- Try to add new cells.
- Try to change the type of a cell.
- Try some Markdown in a Markdown cell.
- Try some Python in a Python cell. 
- Review the code and see how it works. 

---

## Project 4: Create Your Own Repository and EDA Project from Scratch

This is the important part. 
Create a new project using Jupyter notebooks from scratch (without starting with existing code.)
Follow the steps below. 

## Step 1: Start Project, Open in VS Code

Start a project as usual. 
1. Create a repo in GitHub with a default README.md. 
2. Clone the repo down to a Projects folder on your machine. 
3. Open your new project repository in VS Code.

### Step 2: Add/Update Critical Files

With your new project repo folder open in VS Code, add/update critical project files at the start of every project. 

### Add/Add .gitignore

- The .gitignore file tells Git files to ignore when committing changes.
- Review/copy the example [.gitignore](https://github.com/denisecase/datafun-04-notebooks/blob/main/.gitignore) file, you can use it without modification.

### Add/Update requirements.txt

- The requirements.txt file lists the packages used in the project.
- Review/copy the example [requirements.txt](https://github.com/denisecase/datafun-04-notebooks/blob/main/requirements.txt) file, you can use it without modification.
- You may not use all the listed packages - and may want to add others. Modify the requirements.txt as needed.

### Update README.md

- Edit and customize your README.md to provide an overview of the project and instructions for running it.
 
### Git add-commit-push

After adding .gitignore (or any other key file), run git add, commit, and push to commit your changes to GitHub. 

```shell
git add .
git commit -m "Add .gitignore"
git push -u origin main
```

---

### Step 3: Set up Virtual Environment

Next, create and activate a virtual environment for this project. 
Also install additional dependencies required for this project.
See [requirements.txt](requirements.txt) for detailed instructions. 

A. Create .venv
B. Activate .venv
C. Install dependencies into .venv
D. Select VS Code interpreter to use .venv


### Step 4: Create a Jupyter Notebook and Create/Set Kernel

### Create a new notebook

In VS Code, from the menu, select View / Command Palette.

Type `notebook` and select `Jupyter: Create New Blank Notebook`.
This will create a new notebook in the project folder.

Save the notebook with a name like `yourname-notebook.ipynb`.

### Create a kernel from .venv

In the active virtual environment, create a Python kernel to run our notebooks. 
The following command registers the .venv virtual environment as a kernel, making it accessible in Jupyter.
Choose the correct command for your operating system.

```shell
py -m ipykernel install --user --name .venv --display-name "Python (.venv)"
python3 -m ipykernel install --user --name .venv --display-name "Python (.venv)"
```

Verify the .venv entry appears:

```shell
jupyter kernelspec list
```

### Select the virtual environment for the notebook kernel

In VS Code, select your notebook. 
Then, from the menu, select View > Command Palette.
Type Notebook: Select Notebook Kernel.
Choose the kernel with our local "Python (.venv)" from the list.

This ensures your notebook uses the packages installed in your virtual environment. 
   
### Step 5: Create Your Notebook Incrementally
1. Start building your notebook. 
2. Follow the instructions in [docs/EDA.md](docs/EDA.md).
3. As you work, ensure the notebook continues to run without errors. 
4. As you make productive changes, use git add-commit-push to save your progress.
---

## Troubleshooting and Tips
- See [TROUBLESHOOTING.md](docs/TROUBLESHOOTING.md)

## Additional Resources 
- See [RESOURCES.md](docs/RESOURCES.md)


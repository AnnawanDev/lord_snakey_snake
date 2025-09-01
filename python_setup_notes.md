# Python Set-Up

## Set-up
### Creating a Python Virtual Environment
You can use `venv` command to create a virtual environment inside a project folder, as follows:
```
~ % python3 -m venv some_project/some_project-venv
```

### Activating a Python Virtual Environment
To activate the virtual environment we created in the previous step, run the following command.
```
~ % source some_project/some_project-venv/bin/activate
```

### Installing Packages in a Python Virtual Environment
* in virtual environment, only pip and setup tools are installed by default
* use `pip  list` to see installed tool
* Before we want to use pip to install any packages, let’s upgrade it to the latest version. Since we’re working inside the virtual environment, the following command only upgrades the pip tool inside this environment, not in the other virtual environments or system-wide.
```
python3 -m pip install --upgrade pip
```

### Reproducing a Python Virtual Environment
* `pip freeze` - To create identical environments, you first need to list all the dependencies installed in the project's virtual environment 
* The next step is exporting the package list into the requirements.txt file,
```
pip freeze > requirements.txt
```
* someone reproducing a virtual environment would create a virtual environment, activate it, and then run the `pip install -r requirements.txt` command to install all the required packages.
```
~ % python3 -m venv prj/venv
~ % source prj/venv/bin/activate
(venv) ~ % pip install -r requirements.txt
```

### Deactivating a Python Virtual Environment
*  Once you are done working with a virtual environment, or you want to switch to another virtual environment, you can deactivate an environment by running this command:
```
(alpha-venv) ~ % deactivate
```
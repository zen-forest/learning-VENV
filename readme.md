# VENV

## What is VENV?
A VENV (Virtual environment) is a tool used to isolate specific Python environments on a single machine, allowing you to work with multiple versions of Python and packages without conflict. A VENV is something that can be thrown away and rebuilt easily. 

## Benefits of using a VENV:
* Multiple Python projects with different versions of Python and packages. The ability to work on them without worrying about conflict. 
* Easily switch between environments by activating the virtual environment you want to use. 
* You can create a requirements.txt file that lists the packages and their specific versions, and use this file to set things up on a different machine or production environment. 

## How does a VENV work? 

## How to set a VENV up:
Use the 'venv' module that comes with Python 3. 
```
python3 -m venv myenv
```
This will create a directory called 'myenv' in the current directory. To activate the virtual environment, you can use the 'source' command followed by the path to 'activate' the script in the environment 'bin' directory like this:
```
source myenv/bin/activate
```

## Installing packages 
Show all current packages
```
pip list 
```

Print the text in the correct format we'd use for a requirements.txt file
```
pip freeze
```

Automatically print output from 'pip freeze' to requirements.txt
```
pip freeze > requirements.txt
```


## How to deactivate VENV
After activating the enviroment, you can install using 'pip' and packages will be installed in the virtual environment rather than the global one. When you're done, you can deactivate the VENV by running: 
```
deactivate
```

## How to delete a VENV
```
rm -rf venv 
```

## How to install packages from a new VENV
```
pip install -r requirements.txt

```

## Can you have multiple versions of a VENV in a project? 
Yes. This can be helpful when testing different versions of Python or packages. 
```
python3 -m venv env1
python3 -m venv env2
```
```
source env1/bin/activate
source env2/bin/activate

```
## Gotchas
* Don't commit your venv to source control (include requirements.txt)
* Don't put any project files in your venv folder
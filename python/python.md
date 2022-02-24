# Python

## PYTHONPATH environment variable
The name is case sensitive in Ubuntu (not like in Windows). It must be __PYTHONPATH__. See [ubuntu.md](../ubumtu/ubuntu.md) for how to create environment variable. The PYTHONPATH may have multiple folders. 
```
PYTHONPATH=path_to_folder1:path_to_folder2:......:path_to_foldern
```
But it is a single namespace so there should be no duplicated packages or modules in those folders.

## Set PYTHONPATH in .venv environment

open .venv.pyvenv.cfg file, add pythonpyth property in it, and then restart VS Code to make change active.
```
pythonpyth = ....
```


## Find installation location of pip
```
pip show pip
```

## Using virtual env in python3
1. Create virtual env in project home directory
```
# in project home directory
python3 -m venv .venv
```
2. Activate virtual env
```
source .venv/bin/activate
# if activate is not executable, then
chmod 777 .venv/bin/activate
```
3. Install project dependencies if there is requirements.txt
```
pip install -r requirements.txt
```
4. If VSCode does not automatically selects the virtual env, press ^Shift+^Ctrl+P keys to select it
5. remove virtual evn. remove .venv directory.
```
rm -rf .venv
```

## Using virtualenv with python2
1. install virtualenv
```
sudo apt install virtualenv
```
2. create virtual env in project home with config _env2_
```
virtualenv --python=python2 env2
```
3. activate virtual env
```
source env2/bin/actiate
```
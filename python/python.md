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

## Change Project Home Directory Name
After change project home directofy
1. Change old project path to new project path in PYTHONPATH
2. In <project-home>/.venv/bin/activate, change the value of __VIRTUAL_ENV__ from old project path to new project path
3. In <project-home>/.venv/bin/pip file, change the first line, which bash script uses to determine the python used by the project
```
from
#!/home/john/git/python-ml/<old-project-name>/.venv/bin/python3
to
#!/home/john/git/python-ml/<new-project-name>/.venv/bin/python3
```
An altertive way, which will avoid to make any configuration change, is 
1. copy *project* to *project (copy)*
2. delete *project*
3. change *project (copy)* back to *project*

## Find installation location of pip
```
pip show pip
```

## Using virtual env in python3
1. Create virtual env in project home directory, then run one of *python3* or *python* command
```
# in project home directory
python3 -m venv .venv 
python -m venv .venv
```
2. Activate virtual env. This is for Linux only
```
source .venv/bin/activate
# if activate is not executable, then
chmod 777 .venv/bin/activate
```
3. Activate even. The command may be different. In Linux, the script **activate** is in **.venv/bin**. But it may be in **.venv/Scripts** in windows

    * In Linux, run
    > source .venv/bin/activate
    * In Windows, run
    > .venv\Scripts\activate

4. Install project dependencies if there is requirements.txt or using **pip** manully.
> pip install -r requirements.txt

5. If VSCode does not automatically selects the virtual env, press ^Shift+^Ctrl+P keys to select it
6. remove virtual evn. remove .venv directory.
> rm -rf .venv

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
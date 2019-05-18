[https://realpython.com/python-modules-packages/](https://realpython.com/python-modules-packages/)

## Which python.exe will invoke first
1. python.exe in the current directory.
2. python.exe in OS PATH environment variable.

## Module search path
1. The directory from which the input script was run or the current directory if the interpreter is being run interactively.
2. The list of directories in PATHONPATH environment variable if it is set.
3. An installation-dependent list of directories configured at the time Python is installed. 

The code below displays the search path where C:\\Apps\\Anacoda3 is the current directory and no PATHONPATH environment variable
```
>>> import sys
>>> sys.path
['',
 'C:\\Apps\\Anaconda3\\python37.zip',
 'C:\\Apps\\Anaconda3\\DLLs', 
 'C:\\Apps\\Anaconda3\\lib',
 'C:\\Apps\\Anaconda3',
 'C:\\Apps\\Anaconda3\\lib\\site-packages',
 'C:\\Apps\\Anaconda3\\lib\\site-packages\\win32',
 'C:\\Apps\\Anaconda3\\lib\\site-packages\\win32\\lib',
 'C:\\Apps\\Anaconda3\\lib\\site-packages\\Pythonwin']
```

## Add search path programmatically
```
sys.path.insert(0, '../imglib')
sys.path.append(r, 'c:\Users\lib')
```

## Display module path
```
>>> import re
>>> re.__file__
'C:\\Python36\\lib\\re.py'
```

## Display the list of names defined in module using dir()
1. Current module 
```
>>> dir()
['__annotations__', '__builtins__', '__doc__', '__loader__', '__name__',
'__package__', '__spec__']
```
2. Named module
```
>>> import mod
>>> dir(mod)
['Foo', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__',
'__name__', '__package__', '__spec__', 'a', 'foo', 's']
```

## Package initialization __init__.py
1. Create __init__.py in the package directory.
2. Define package level variable and execute code when package first imported

## Display current working directory
```
import os
os.getcwd()
```

## Install spellchecker for Jupyter Notebook
```
pip install jupyter_contrib_nbextensions
jupyter contrib nbextension install <--user>
jupyter nbextension enable spellchecker/main
```
Note:

* *--user* is optional.
* pip install the package to default environment. Look in installation process output for the location.

## Find installed package location
```
pip show <package name>
```

## List pip installed packages
```
pip list
```

## How to find python installed directory
```
$ python
Python 3.7.2 (tags/v3.7.2:9a3ffc0492, Dec 23 2018, 23:09:28) [MSC v.1916 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> import sys
>>> sys.executable
'C:\\Users\\user\\AppData\\Local\\Programs\\Python\\Python37\\python.exe'
```
Note: Anaconda and its environments use different python installed directories. To see it
1. Select environment
2. Select Open with Python
3. Type 
```
>>> import sys
>>> sys.executable
'C:\\Apps\\Anaconda3\\envs\\Image and Video\\python.exe'
```
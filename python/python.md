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
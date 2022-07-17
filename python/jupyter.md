# Jupyter

## installation
1. Activate project environment. for example
> source .venv/bin/activate
2. Upgrade pip. (The python3 installation process will install pip3, but it does not include _pip_. Verify it by checking if _.venv/bin_directory has _pip_ file. The _Upgrade pip_ command will also create _pip_ file)
> pip3 install --upgrade pip
3. Install _jupyter_ 
> pip install jupyter
4. At this time, _jupyter_ is installed in the .venv, when starting _jupyter notebook_ with command below, all packages in _.venv_ are available in _jupyter notebook_
> jupyter notebook
# Google Colab

## Mount Google Drive to Colab

1. run python Jupter cell
```
from google.colab import drive
drive.mount('/content/gdrive')
```
2. in the popup window, select account to connect and allow access. 'Mounted at /content/gdrive' will display in output

3. type the bash command below to verify mounted google drive
```
# verift gdrive is in root
!ls -l
# verify gdrive has the correct content of google drive
!ls -l gdrive/*
``` 
Note: when connection lost, the mounted drive lost too. when reconnecting, go through the steps above to re-mount google drive

## Add File to Python Path for Import in Jupyter Nodebook
This is Jupyter Nod
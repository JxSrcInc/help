To draw China map with province level administration information (adm1) using Basemap, you must follow the steps below to download China's shapefile and put them into a working directory

1. Go to [http://www.diva-gis.org/gdata](http://www.diva-gis.org/gdata) web site.
2. Select China in Country.
3. Select Administrative areas in Subject. It should be the first choice in dropdown list. If not, select it.
4. Click OK to download. The downloaded file name should be CHN_adm.zip
5. Create CHN_adm directory in the application Home directory. If you use Jupyter Notebook, create CHN_adm directory in Jupyter Notebook root directory. you can use the command "%pwd" to find it
6. Extract downloaded CHN_adm.zip file to that directory.
7. You must run 'matplotlib inline' in Jupyter Notebook after extracting files from CHN_adm.zip.
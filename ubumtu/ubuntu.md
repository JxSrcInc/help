
# Ubuntu

## Install Ubunto 20.4

check add Wifi option no matter choose standard (recommended) minimal installation. If not, Wifi driver will not be available. To install Wifi driver, wired connection is required.

## List package
```
dpkg --list | grep <package name>
```

## Grep: ignore word, UPPER and LOWER
```
grep -i <pattern>
```

## Print environment variables
```
printenv
```

## Create environment variable in user environment
open *__.bashrc__* file in user home folder and add export statement as below.
```
export variable-name=variable-value
```
NOTE: Environment variable name is case sensitive (not like Windows where it is not case sensitive). Must relogin as user to make added environment variables active.

## locate utility
```
locate <module name>
```

## USB 
When USB connected to this laptop, the mount name should show in left list in Files. Its parent folder is __/media/john__. If the mount name is __UUI__, then the path to USB is
```
/media/john/UUI
```

## Check disk space
```
df -h
```

## Create desktop shotcut

Example: anaconda

1. create anaconda.desktop file in ~/Desktop
2. copy anaconda.desktop to ~/.local/share/applications
3. click shotcut image/icon in desktop GUI and allow launtch it 

## Create screen shot
1. Print Screen to take a screenshot of the desktop.
2. Alt + Print Screen to take a screenshot of a window.
3. Shift + Print Screen to take a screenshot of an area you select.

Use __screenshots__ application to select how to save screenshot.

1. Open/Click __Activities__
2. Type 'screenshots' in search to find and open __screenshots__ application. (You will see the application when just type 1 (s) or 2 (sc) letter)
3. Select how to make screenshot
4. Before __screenshots__ completes its work, it will promotes a windor for you to choose _copy to clickboard_ or _save_. Under _save_ option, you can specify where to save the screenshot. The default folder to save screenshot is Picture.


## Install Google online account
1. Open ubuntu _Settings_
2. Select _Online Accounts_ 
3. Select _Google_ under _Add an account_
<img src='GNOME.png'>
4. Follow instruction to complete work

## [Stop and Update _Snap Store_](https://askubuntu.com/questions/1430194/how-to-stop-snap-store-for-update)
```
snap-store --quit
sudo snap refresh
```

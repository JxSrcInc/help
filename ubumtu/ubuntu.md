
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

## Install Google online account
1. Open ubuntu _Settings_
2. Select _Online Accounts_ 
3. Select _Google_ under _Add an account_
<img src='GNOME.png'>
4. Follow instruction to complete work

## Allow Remote Access
enable firewall
> sudo ufw enable
check firewall status
> sudo ufw status

## update node.js
node.js includes system dependent files. In Windows, delete the old version and install the version you want.
1. open Windows Settings -> Apps, and delete old node.js
2. download new version from [https://nodejs.org/en/
](https://nodejs.org/en/)
3. run the downloaded _node-xxx.msi_ file to install node.js


## npm install directory
> npm list -g

The first line shows the directory which contains all packages npm installed. In Windows, it is _C:\Users\\<user\>\AppData\Roaming\npm_
## update npm
> npm update npm

this command updates all packages installed in npm install directory - the directory showed in _npm list -g_ command.


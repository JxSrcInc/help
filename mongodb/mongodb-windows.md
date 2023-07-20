# Mongo DB on Windows

## start server from command line
1. add mongod.exe to Path environment
2. create mongodb directory. for example, c:\git\ml-stock\mongod\data
3. start run mongod
```
# default port 27017
mongod --dbpath c:\git\ml-stock\mongod\data

# or using different port
mongod --dbpath c:\git\ml-stock\mongod\data --port 27019

```

## stop server
close the terminal

## use mongosh
```
mongo
```

## create windows service for mongod
See [web site](https://medium.com/stackfame/run-mongodb-as-a-service-in-windows-b0acd3a4b712)

Default mongod configuration is at <mongod-install-dir>\Server\<version>\bin\mongod.cfg. it is used for windows mongod service with default port 27017. Copy, modify it, and uses it as it as config file for windows mongod service with different port.

To create windows server, run command below in CLI

> mongod --config <path-to>mongod.cfg install

View, stop and restart windows service
1. click Windows + R keys. it opens windows search
2. in search box, type
>  services.msc
3. do task in Service dialog window. 

## Backup and Restore

1. import _Quotes.json_ from current directory to collection _Quotes_ in db _quote_
```
mongoimport --collection=Quotes --db=quote --drop --file=Quotes.json
```

2. export collection _Quotes_ from db _quote_ to _Quotes.json_ in current directory
```
mongoexport --collection=Quotes --db=quote --out=Quotes.json
```

3. export db _symbol_ to default _dump_ directory (_dump/symbol_). repeat the command below with different db, for example, min5Quote. it will create _min5Quote_directory in _dump_. When completed to dump all dbs, copy _dump_ to the machine for restore
```
mongodump --db symbol
```

4. import from default _dump_ directory. go to the parent directory of _dump_ directory, then symply run mongorestore
```
mongorestore 
```


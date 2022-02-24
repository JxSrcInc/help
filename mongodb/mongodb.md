# Mongo DB

## start server from command line
```
sudo systemctl enable --now mongod
# or
sudo systemctl start mongod
# restart (stop then start)
sudo systemctl restart mongods
```

## check server status
```
sudo systemctl status mongod
```
## default port 27017
to verify
```
sudo netstat -tunelp | grep 27017
```
## installed directories
```
/var/lib/mongodb
/var/log/monogdb        #log
/etc/mongod.conf        # config file
```
## stop server
```
sudo service mongod stop
```
## use mongosh
```
mongo
```

## create second db instance
The instruction below is based on web [link](https://medium.com/@akshay2gud/creating-multiple-instances-of-mongodb-on-server-and-setting-replication-of-database-5ead59e1e4d4) but modified according to local configuration

1. create database path
```
cd /var/lib
sudo mkdir mongodb1
chown mongodb:mongodb mongodb1
```
2. create log
```
cd /var/log
sudo mkdir mongodb1
chown mongodb:mongodb mongodb1
```
3. create new config file
```
cd /etc
sudo cp mongod.conf mongod1.conf
```

4. modify mongod1.conf
    1. sudo gedit mongod1.conf
    2. In storage.dbPath: /var/lib/, change mongodb to mongodb1
    3. In systemLog.path /var/log change /mongodb/ to /mongodb1/
    4. In net.port, change 27017 ti 27018


5. create new service for mongodb1
```
cd /lib/systemd/system
sudo cp mongod.service mongod1.service
```
6. edit mongod1.service
    1. sudo gedit mongod1.service
    2. change mongod.conf to mongod1.conf in ExecStaraat
    ```
    ExecStart=/usr/bin/mongod --config /etc/mongod1.conf
    ```

7. deploy process
```
sudo systemctl start mongod1.service
```
8. check new server status
```
sudo systemctl status mongod1
```
9. open mongo and connect to mongod1
```
mongo --host 127.0.0.1 --port 27018
```

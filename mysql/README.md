# Account information

## root
```
    user: root
    pwd:  123
```

## cza
```
    user: cza
    pwd:  123
    grantDB: czatest1
```

# Start

## create user and grant authority
```
mysql> CREATE USER 'cza'@'%' IDENTIFIED BY '123';
mysql> create database czatest1;
mysql> grant select,insert,update,delete,create,drop on czatest1.* to cza@'%' IDENTIFIED BY '123';
```

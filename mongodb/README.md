# Account information

## admin
```
    user: cza
    pwd:  123
```

## sunteng::bidex
```
    user: sunteng_bidex
    pwd:  mongo-bidex2017.cn
    grantDB: sunteng_bidex
```


# Start

## create user and grant authority
```
> db.createUser({user: 'cza', pwd: '123', roles: [{role: "userAdminAnyDatabase", db: "admin"}, {role: "readWriteAnyDatabase", db: "admin"}]});
> db.auth('cza', '123');
> use sunteng_bidex
> db.createUser({user: 'sunteng_bidex', pwd: 'mongo-bidex2017.cn', roles: ["readWrite"]});
```

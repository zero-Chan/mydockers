# Account information


# Start
## Check OK or not
```shell
docker exec -it etcd-3.2.7-1 /bin/sh
etcdctl --endpoints=127.0.0.1:2479 member list
```
if is ok, output
```
8aa2ba79b4cae189, started, etcd-node-1, http://127.0.0.1:2480, http://127.0.0.1:2479
ba2ae674ab618960, started, etcd-node-2, http://127.0.0.1:2580, http://127.0.0.1:2579
cd652a5796ee30a3, started, etcd-node-3, http://127.0.0.1:2680, http://127.0.0.1:2679
```

## Test 
set and get value to etcd cluster
```shell
docker exec -it etcd-3.2.7-1 /bin/sh
etcdctl put foo 1 --endpoints=127.0.0.1:2479
exit
docker exec -it etcd-3.2.7-2 /bin/sh
etcdctl get foo --endpoints=127.0.0.1:2579
exit
```

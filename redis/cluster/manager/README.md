# Build redis-cluster-manager docker image
```shell
make
```

# Example: create redis-cluster
```shell
docker run -it --network=host redis-cluster-manager:1 create --replicas 1 127.0.0.1:10381 127.0.0.1:10382 127.0.0.1:10383 127.0.0.1:10384 127.0.0.1:10385 127.0.0.1:10386
```

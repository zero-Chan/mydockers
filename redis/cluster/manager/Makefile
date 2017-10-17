docker_respository=redis-cluster

resposition_tag=1

manager_docker_full_respository="${docker_respository}-manager:${resposition_tag}"

.PHONY: manager
all: manager

manager:
	docker build -t "${manager_docker_full_respository}" .

.PHONY: clean
clean:
	docker rmi "${manager_docker_full_respository}"

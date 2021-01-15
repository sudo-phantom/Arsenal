# Docker-Swarm

## Setup

```docker swarm init```

Start the swarm service

```docker swarm join-token worker```

print the command to add worker to the swarm as worker (Run printed command on worker node)

```docker swarm join-token manager```

print the command to add worker to the swarm as manager (Run printed command on manager node)


## Service

```docker node ls```

List the nodes in the swarm

```docker service create <image_name> <command>```

Start a 1 node cluster and run a single command

```docker service ps <service_name>```

List information on a service

```docker service update <service_name> --replicas 3```

Increase number of nodes to 3
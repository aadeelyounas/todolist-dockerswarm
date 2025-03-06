# Scaling the ToDo Application

This document provides instructions on how to scale the ToDo application services in a Docker Swarm environment.

## Scaling Services

To scale a service, use the following command:

```
docker service scale <service-name>=<number-of-replicas>
```

For example, to scale the `api` service to 3 replicas, use the following command:

```
docker service scale my-stack_api=3
```

To scale the `frontend` service to 5 replicas, use the following command:

```
docker service scale my-stack_frontend=5
```

To scale the `db` service to 2 replicas, use the following command:

```
docker service scale my-stack_db=2
```

## Verifying the Scale

To verify the scale of a service, use the following command:

```
docker service ps <service-name>
```

For example, to verify the scale of the `api` service, use the following command:

```
docker service ps my-stack_api
```

This will show the status of each replica of the service.

## Scaling Down Services

To scale down a service, use the same command as above, but with a smaller number of replicas.

For example, to scale the `api` service down to 1 replica, use the following command:

```
docker service scale my-stack_api=1
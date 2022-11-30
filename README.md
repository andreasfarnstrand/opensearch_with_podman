# OPENSEARCH AND OPENSEARCH_DASHBOARDS WITH PODMAN
Creates and run an instance of opensearch and opensearch dashboard.
This needs podman-compose to be installed.
Visit https://github.com/containers/podman-compose to learn how to install this.

Ofcourse this works just as well with docker and docker-compose.

## 1. Build a new dashboard
This disables the security plugin and builds a new image
tagged opensearch-dashboards-no-security.
cd into the cloned directory
```
podman build --tag=opensearch-dashboards-no-security .
```

## 2. Run podman-compose
This uses the new dashboard image previoudly built.
Starts the containers in detached mode.
```
podman-compose up -d
```

## 3. Visit localhost:5601
Goes to the new Opensearch dashboard.

## Stoping
To stop and remove containers
```
podman-compose down
```
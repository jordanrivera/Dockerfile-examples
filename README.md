# Dockerfile-examples

"With Docker, developers can build any app in any language using any toolchain. “Dockerized” apps are completely portable and can run anywhere - colleagues’ OS X and Windows laptops, QA servers running Ubuntu in the cloud, and production data center VMs running Red Hat.

Developers can get going quickly by starting with one of the 13,000+ apps available on Docker Hub. Docker manages and tracks changes and dependencies, making it easier for sysadmins to understand how the apps that developers build work. And with Docker Hub, developers can automate their build pipeline and share artifacts with collaborators through public or private repositories.

Docker helps developers build and ship higher-quality applications, faster." --

# Check Version

It is very important that you always know the current version of Docker you are currently running on at any point in time. This is very helpful because you get to know what features are compatible with what you have running. This is also important because you know what containers to run from the docker store when you are trying to get template containers. That said let see how to know which version of docker we have running currently.

* docker version   Shows which version of docker you have running.
* docker version --format '{{.Server.Version}}' Get the server version

Starting and Stopping

* docker start Starts a container so it is running.
* docker stop Stops a running container.
* docker restart Stops and starts a container.
* docker pause Pauses a running container, "freezing" it in place.
* docker unpause Will unpause a running container.
* docker wait Blocks until running container stops.
* docker kill Sends a SIGKILL to a running container.
* docker attach Will connect to a running container.

If you want to detach from a running container, use Ctrl + p, Ctrl + q. If you want to integrate a container with a host process manager, start the daemon with -r=false then use docker start -a.

# Lifecycle

* docker create Creates a container but does not start it.
* docker rename Allows the container to be renamed.
* docker run Creates and starts a container in one operation.
* docker rm Deletes a container.
* docker update Updates a container's resource limits.

# Info

* docker ps Shows running containers.
* docker logs Gets logs from container. (You can use a custom log driver, but logs is only available for json-file and journald in 1.10).
* docker inspect Looks at all the info on a container (including IP address).
* docker events Gets events from container.
* docker port Shows public facing port of container.
* docker top Shows running processes in container.
* docker stats Shows containers' resource usage statistics.
* docker diff Shows changed files in the container's FS.
* docker ps -a Shows running and stopped containers.

docker stats --all shows a list of all containers, default shows just running.

# Import / Export

* docker cp Copies files or folders between a container and the local filesystem.
* docker export Turns container filesystem into tarball archive stream to STDOUT.

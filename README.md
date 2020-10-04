# ansible-bind
Deploy docker container with BIND-server based on sameersbn/bind

## Role variables
    Variable                    |       Default value           |      Description
--------------------------------|-------------------------------|---------------------------------------    
bind_service_name               |       bind-docker             |   Service name in OS
uninstall_service               |       false                   |
bind_host_port                  |       53                      |   Host network port for service
bind_container_port             |       53                      |   Container network port for service
bind_port_type                  |       udp                     |   Type of port (tcp/udp) for service
bind_web_host_port              |       10000                   |   Host network port for service management (http)
bind_web_container_port         |       10000                   |   Container network port for service management (http)
bind_web_port_type              |       tcp                     |   Type of port (tcp/udp) for service management (http)
host_dir                        |       /var/docker/bind        |   Mapping directory on host
container_dir                   |       /data                   |   Mapping directory on container
docker_image                    |       sameersbn/bind          |   Docker image (https://hub.docker.com/)
---------------------------------------------------------------------------------------------------------

### How to use
    - installation: just start the role
    - uninstallation: add --extra-vars "uninstall_service=true" (WARNING: It doesn't delete configs on host!!!)
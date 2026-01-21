# openvpn-docker
[![docker-hub Actions Status](https://github.com/dachack/openvpn-docker/workflows/docker-hub/badge.svg)](https://github.com/dachack/openvpn-docker/actions)

Run openvpn on latest Alpine in Docker

## About
If you simply want to use OpenVPN in a Docker container without additional bloat I found it hard to find something suitable and decided to build this workflow. Nothing special and a very naive, simplistic approach. Please let me know in case I missed something important.
* Provide existing OpenVPN config folder as volume or create a new one based on [OpenVPN Reference](https://openvpn.net/community-resources/reference-manual-for-openvpn-2-4/)
* Provide existing certificate as volume, e.g. included in OpenVPN config folder (be careful with permissions!) and link in .conf-File
* Run this container that utilizes minimalistic, yet up-to-date software (OS and OpenVPN-package), e.g. by using Portainer and/or the Docker-Compose below
* Use Watchtower to regularly update the base image for your container

## Host setup
Make sure you have port forwarding activated in the kernel.

Allow forwarding from and to the tunnel in your firewall, e.g.:
```
View older version to see this code
```
And -if everything works as expected - install iptables-persistent to make sure these settings survive a reboot:
```
View older version to see this code
```

## Image on Docker Hub
https://hub.docker.com/r/dachack/openvpn

## Sources in Github
https://github.com/DaCHack/openvpn-docker

## Docker-compose
```
View older version to see this code
```

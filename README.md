# podman-secure-nginx-proxy

Nginx reverse proxy with Let's encrypt auto-renew SSL cert, WAF support, fail2ban and auto-gen reverse proxy config for new backend applications optimized for podman

## why this repo?

On RHEL7 / CentOS 7 docker was the default container builder/runtime and I heavily used jwilder/nginx-proxy
with his beautiful [docker-gen][1] for [Automated Nginx Reverse Proxy for Docker][2].

Non on RHEL8/ CentOS 8 things have changed, podman is the default container runtime and which has different API and no UNIX sockets for interaction.

This repo will set up a similar "Automated Nginx Reverse Proxy mechanism" using podman.

Also it will add optional features from other popular repositoies such as automatic SSL renewal using Let's encrypt and a bit of fail2ban for Nginx.

[1]: https://github.com/jwilder/docker-gen
[2]: http://jasonwilder.com/blog/2014/03/25/automated-nginx-reverse-proxy-for-docker/

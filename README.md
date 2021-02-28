# podman-secure-nginx-proxy

Nginx reverse proxy container optimized for Podman with auto-gen of reverse proxy config for automatically adding backend systems without Nginx restart. Optional features such as Let's encrypt auto-renew SSL cert, WAF support and fail2ban can be enabled too.

## why this repo?

On RHEL7 / CentOS 7 docker was the default container builder/runtime and I heavily used jwilder/nginx-proxy
with his beautiful [docker-gen][1] for [Automated Nginx Reverse Proxy for Docker][2].

Non on RHEL8/ CentOS 8 things have changed, podman is the default container runtime and which has different API and no UNIX sockets for interaction.

This repo will set up a similar "Automated Nginx Reverse Proxy mechanism" using podman.

Also it will add optional Nginx features from other popular repositoies such as automatic SSL renewal using Let's encrypt, modsecurity and a bit of fail2ban to make your reverse proxy a bit more secure and production ready.

[1]: https://github.com/jwilder/docker-gen
[2]: http://jasonwilder.com/blog/2014/03/25/automated-nginx-reverse-proxy-for-docker/

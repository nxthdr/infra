# Infrastructure 

## iptables

By default, docker network bridges are not accessible from the outside world.  
We simply accept any traffic from the DMZ network.

```sh
ip6tables -I DOCKER-USER -d 2a06:de00:50:cafe:100::/80 -j ACCEPT
```
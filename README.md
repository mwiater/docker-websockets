# Node.js WebSocket example in Docker

Baeds off of this example, but made to work as a Swarm Service: https://github.com/lrutten/docker-nodejs-ws

```
docker service create \
--name wsserver \
--publish 8080:8080 \
--publish 80:80 \
--constraint=node.labels.type==websockets \
mattwiater/websockets
```

#### To Do
* Work on volumes for persistant storage (i.e.: rexray, flocker, etc.)

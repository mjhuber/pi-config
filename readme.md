# raspberry pi setup

1.  create the overlay networks
```
docker network create frontend && docker network create backend
```

2.  Enable systemd services
```
find /usr/local/docker/* -maxdepth 0 -type d | sed 's/.*\///' | xargs -i{} systemctl enable docker-compose@{}
```

3.  Start services
```
find /usr/local/docker/* -maxdepth 0 -type d | sed 's/.*\///' | xargs -i{} systemctl start docker-compose@{}
```

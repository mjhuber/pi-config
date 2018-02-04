# raspberry pi setup

1.  Enable systemd service
```
find /usr/local/docker/* -maxdepth 0 -type d | sed 's/.*\///' | xargs -i{} systemctl enable docker-compose@{}
```
2.  Start services
```
find /usr/local/docker/* -maxdepth 0 -type d | sed 's/.*\///' | xargs -i{} systemctl start docker-compose@{}
```

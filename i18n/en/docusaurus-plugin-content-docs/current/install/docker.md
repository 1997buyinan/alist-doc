---
sidebar_position: 5
---

# Use Docker

See the log output for the initial password:
```bash
docker logs alist
# or
docker exec -it alist ./alist -password
```

### stable version
```bash
docker run -d --restart=always -v /etc/alist:/opt/alist/data -p 5244:5244 --name="alist" xhofe/alist:latest
```

### beta version
Not recommended, this may can't work properly
```bash
docker run -d --restart=always -v /etc/alist:/opt/alist/data -p 5244:5244 --name="alist" xhofe/alist:v2
```

### Specify version
See https://hub.docker.com/r/xhofe/alist for details
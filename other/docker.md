# Docker



## Add host network to container

```yaml
services:
  rabbitmq:
    container_name: rabbitmq
    image: rabbitmq:3.11.16-management
    restart: unless-stopped
    extra_hosts:
      - "host.docker.internal:host-gateway"
```

You can access to host with `host.docker.internal` domain name.
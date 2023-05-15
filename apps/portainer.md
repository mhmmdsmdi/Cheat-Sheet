# Portainer - Container management software for Docker and Kubernetes

## Installation

Create volume:

```cmd
docker volume create portainer_data
```

Run the image:

```bash
docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest
```

Lunch at [https://localhost:9443](https://localhost:9443)
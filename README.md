# Prisma Cloud Compute Edition - Console Deployment
This repository contains different ways to customize your Prisma Cloud Compute Edition deployment on other platforms outside of what `twistcli` provides.

## Requirements
You need to load the container image of the Console to a private registry to be able to pull it down across multiple deployments.
```bash
docker load -i prisma_cloud_compute_edition-<VERSION>.tar.gz
```

### Docker Compose
Using Compose, multiple supervisor consoles can be deployed on a single host using project names.
```bash
docker compose -p prod up -d
docker compose -p test up -d
```

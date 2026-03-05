# Kong Gateway Deployment

This directory contains Kubernetes manifests for Kong Gateway deployment.

## Current Version
- Kong Gateway: 3.13.0.1
- Kong Ingress Controller: 3.5
- PostgreSQL: 15

## Structure
- `base/` - Base Kubernetes manifests
- `argocd-app.yaml` - ArgoCD Application definition

## Access
- Kong Admin API: http://kong-admin.abu7midan.com
- Kong Manager: http://kong-manager.abu7midan.com
- Kong Proxy: http://kong-proxy.abu7midan.com

## Configuration
- Database: PostgreSQL (kong-postgresql.kong.svc.cluster.local)
- Admin Password: admin (change in production!)
- Enterprise features enabled

## Maintenance
To update Kong version, modify the image tag in `base/deployment.yaml`:
- `kong/kong-gateway:3.13.0.1` - Kong Gateway
- `kong/kubernetes-ingress-controller:3.5` - Ingress Controller

## ArgoCD
This application is managed by ArgoCD. Any changes pushed to this directory will be automatically synced to the cluster.

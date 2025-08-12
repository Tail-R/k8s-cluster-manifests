# Project Title

Manifests for High Availability Game Server Setup

## Purpose

This project aims to improve the availability and maintainability of game server instances by declaratively describing their desired state, decoupling it from the underlying physical infrastructure.

## Features

- Instant server creation based on manifests
- Kubernetes ensures idempotent cluster state management
- Stateful session maintenance and load balancing
- Enhances scalability by separating physical and logical layers

## How to Use

These manifests are primarily intended to be adapted from configuration management tools such as Ansible and Terraform. Alternatively, you can apply them directly by running the following command:

```bash
kubectl apply -k github.com/Tail-R/k8s-cluster-manifests/overlays/dev?ref=dev
```

## Notes

- Currently, only simple round-robin load balancing is supported; load balancing based on pod load is not available.
- Envoy redundancy is not implemented, resulting in a single point of failure.

## License

MIT
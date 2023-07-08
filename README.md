# boot-project-gitops

Helm Chart to help create the OpenShift projects based on good practices and out of the box OpenShift features.

Use this Helm Chart with ArgoCD when practicing "Everything as Code" using GitOps.

- https://github.com/eformat/boot-project
- https://github.com/eformat/boot-project-values

This repo contains the setup and per-cluster, gitops argocd files.

## Setup

Setup ACM and Cluster-Scoped ArgoCD

```bash
oc apply -f bootstrap-acm-global-gitops/setup.yaml
```

## Bootstrap Projects

```bash
oc apply -f applications/boot-projects-appset.yaml
```

## Label Clusters

- Label you cluster with `boot-projects-dev=true` to setup dev projects

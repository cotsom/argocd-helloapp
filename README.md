# argocd-helloapp — template for deploying a Pod that runs commands inside the k8s cluster

This repository is a **minimal template** that deploys a Kubernetes **Pod** which executes a command inside the cluster. It includes two deployment options so you can pick what ArgoCD supports in your environment:

* `kustomize/` — plain `kustomization` with `pod.yaml`

* `helm/` — minimal Helm chart (`Chart.yaml`, `values.yaml`, `templates/pod.yaml`)

## kustomize
The command is specified in `kustomize/pod.yml`
```bash
command: ["/bin/sh", "-c", "echo Hello from Pod && sleep 20 && echo done"]
```

## helm
The command is specified in `helm/values.yaml`

```yaml
command: "echo Hello from Helm && sleep 20 && echo done"
```
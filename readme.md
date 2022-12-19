Workflows & Events Demo

Add `--enable-helm` for kustomize.

Apply [`app-of-apps.yaml`](./app-of-apps.yaml)
- Will need to adjust destination to your own cluster. 
- Assumes connected cluster arch (e.g., Akuity)

Connect to workflows and minio:
- `kubectl -n argo port-forward deployment/argo-server 2746:2746`
- [`localhost:2748`](https://localhost:2748) (requires using HTTPS)
  - No log in required thanks to auth-mode patch.

Connect to minio:
- `kubectl port-forward svc/minio-console 9001 -n minio`
- [`localhost:9001`](http://localhost:9001)

Update values in `apps/patch-argo-application.yaml`
get password from `events/secret-artifact-minio.yaml`

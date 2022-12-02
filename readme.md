Workflows & Events Demo

Connect to workflows:
- use HTTPS
- `kubectl -n argo port-forward deployment/argo-server 2746:2746`
- No log in required thanks to auth-mode patch.

kubectl -n argo port-forward deployment/argo-server 2746:2746
kubectl port-forward svc/minio-console 9001 -n minio

Update values in `apps/patch-argo-application.yaml`

get password from `events/secret-artifact-minio.yaml`

Apply app-of-apps
`app-of-apps.yaml`
- Assumes connected cluster arch (e.g., Akuity)

Add --enable-helm for kustomize
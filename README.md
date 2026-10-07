# gitops-demo

Desired state for the Session 20 GitOps labs (DevOps Heroes, Rashi / 10389).
Argo CD watches this repository and keeps the cluster in sync with it.

| Folder | Argo CD Application | Namespace |
|---|---|---|
| `07-argocd/app` | `argocd/session20-app.yaml` | `session20` |
| `08-mini-project/app` | `argocd/session20-mini.yaml` | `session20` |

The Application manifests live in `argocd/`, outside the synced paths, and are applied once with
`kubectl apply -f argocd/<file>`. After that, every change is a commit to this repo.

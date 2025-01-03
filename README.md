### helm

- helm lint skillcode-helm-chart/
- helm install --dry-run skillcode-release skillcode-helm-chart/

### argoCD

- kubectl port-froward -n argocd sercive/argocd-service 8080:443
- kubectl get secret -n argocd argocd-initial-admin-secret -o yaml
  - echo M1FrZlczQ29SNHZzdkNOMQ== | base64 --decode


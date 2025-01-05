### helm

- helm install <release-name> ./chart-dir -n <namespace>
- helm lint skillcode-helm-chart/
- helm install --dry-run skillcode-release skillcode-helm-chart/
- helm template skillcode-release ./skillcode-helm-chart -f skillcode-helm-chart/values.yaml -f skillcode-helm-chart/values-cloud.yaml --show-only templates/frontend-deployment.yaml

### argoCD

- kubectl port-forward -n argocd service/argocd-server 8080:443
- kubectl get secret -n argocd argocd-initial-admin-secret -o yaml
  - echo M1FrZlczQ29SNHZzdkNOMQ== | base64 --decode
- kubectl get secret argocd-initial-admin-secret -n argocd -o jsonpath="{.data.password}" | base64 -d
- (login first) argocd repo list

### kubectl

- kubectl apply -f . -n skillcode-manual

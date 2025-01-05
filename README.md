### helm

-helm install <release-name> ./chart-dir -n <namespace>
- helm lint skillcode-helm-chart/
- helm install --dry-run skillcode-release skillcode-helm-chart/

### argoCD

- kubectl port-forward -n argocd service/argocd-server 8080:443
- kubectl get secret -n argocd argocd-initial-admin-secret -o yaml
  - echo M1FrZlczQ29SNHZzdkNOMQ== | base64 --decode
- kubectl get secret argocd-initial-admin-secret -n argocd -o jsonpath="{.data.password}" | base64 -d


### kubectl

- kubectl apply -f . -n skillcode-manual

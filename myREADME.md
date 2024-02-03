# argocd
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
kubectl port-forward svc/argocd-server -n argocd 8080:443
k get secret -n argocd argocd-initial-admin-secret -o yaml
psw: RQVKQfVDcS8IAKSW user: admin
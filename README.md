echo "# ArgoCD"

------------
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/v2.6.2/manifests/install.yaml

------
Change argocd server service from clusterip to nodeport to access its UI
-------------
argocd cluster add kind-dev-cluster --name rancher-desktop
argocd cluster list

# ansible_role_minikube

Playbook role para crear un cluster kubernetes local con minikube.

Testeado con Vagrant + Virtualbox

---
roles:
- docker	
- kubectl
- helm
- minikube 

notas:
- minikube addons enable ingress
- minikube addons enable dashboard
- kubectl -n kubernetes-dashboard port-forward svc/kubernetes-dashboard --address=192.168.0.2 8080:80

- minikube start --nodes 2 -p multinodo
- minikube status -p multinodo
- minikube service list -p multinodo

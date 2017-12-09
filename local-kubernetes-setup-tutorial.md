# Minikube setup
- install kubectl https://kubernetes.io/docs/tasks/tools/install-kubectl/
- setup minikube
- https://github.com/kubernetes/minikube

# Start ninikube
- run
~~~~~
$ minikube start
~~~~~
- The minikube start command creates a "kubectl context" called "minikube". This context contains the configuration to communicate with your Minikube cluster.
- Minikube sets this context to default automatically, but if you need to switch back to it in the future, run:
~~~~~
kubectl config use-context minikube, or pass the context on each command like this: kubectl get pods --context=minikube.
~~~~~

# Start kubernetes web ui dashboard
- to access the Kubernetes Dashboard, run this command in a shell after starting Minikube to get the address:
~~~~~
minikube dashboard
~~~~~

# Minikube setup
- install kubectl https://kubernetes.io/docs/tasks/tools/install-kubectl/
- to setup minikube follow:
- https://github.com/kubernetes/minikube

# Start minikube
- run
~~~~~
$ minikube start
~~~~~
- The minikube start command creates a "kubectl context" called "minikube". This context contains the configuration to communicate with your Minikube cluster.
- Minikube sets this context to default automatically, but if you need to switch back to it in the future, run:
~~~~~
kubectl config use-context minikube
~~~~~
, or pass the context on each command like this: 
~~~~~
kubectl get pods --context=minikube
~~~~~

# Run simple container
~~~~~
$ kubectl run hello-world --image=gcr.io/google_containers/echoserver:1.4 --port=8080
~~~~~
or 
~~~~~
$ kubectl run hello-world --replicas=2 --labels="run=load-balancer-example" --image=gcr.io/google-samples/node-hello:1.0  --port=8080
~~~~~

# Expose deployment
$ kubectl expose deployment hello-world --type=NodePort


# Start kubernetes web ui dashboard
- to access the Kubernetes Dashboard, run this command in a shell after starting Minikube to get the address:
~~~~~
minikube dashboard
~~~~~

# 

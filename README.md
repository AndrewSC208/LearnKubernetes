# Learn Kubernetes
Demo: https://github.com/jleetutorial/kubernetes-demo

1. Basic MiniKub Commands
a. start
    * minikube start

b. deploy a sample kub "deployment" to your local
    * kubectl run hello-minikube --image=gcr.io/google_containers/echoserver:1.4 --port=8080

c. Expose to external network
    * kubectl expose deployment hello-minikube -type=NodePort

d. list pods
    * kubectl get pod

e. Access the sample service
    * curl $(minikube service hello-minikube --url)

f. delete the deployment
    * kubectl delete deployment hello-minikube
    
g. stop 
    * minikube stop
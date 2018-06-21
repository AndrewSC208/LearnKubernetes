# Learn Kubernetes
Demo: https://github.com/jleetutorial/kubernetes-demo

##
1. Install kub

1. Basic MiniKub Commands
a. start
    * minikube start --vm-driver=virtualbox

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
    

## What does a K8s "app" look like?
* "Deployments" are the centeral metaphor for what we'd consider "apps" or "services"
* Deployments are descrived as a collection of resources and references

### First Deployment
* Deploy the Tomcat App Server using the official docker image
* Key Tasks:
    1. Define the deployment
    2. Expose it's services
    3. Deploy it to our cluster
    
* Thee most simple deployment in Kub is a single pod
* A pod is an instance of a container, Deployments can have any number of Pods required to get the job done.


kubectl get service

kubectl port-forward -h

kubectl proxy


### Common Kubectl commands
 * kubectl get pods
 * kubectl get pods [pod name]
 * kubectl expose <type name> <identifier/name> [—port=external port] [—target-port=container-port [—type=service-type]
 * kubectl port-forward <pod name> [LOCAL_PORT:]REMOTE_PORT]
 * kubectl attach <pod name> -c <container>
 * kubectl exec  [-it] <pod name> [-c CONTAINER] — COMMAND [args…]
 * kubectl label [—overwrite] <type> KEY_1=VAL_1 ….
 * kubectl run <name> —image=image
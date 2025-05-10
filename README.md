# Simple Node Express Hello World App


![localhost:4000](/public/images/localhost_4000.png?raw=true "Node & Express")

# Steps :
```
  git clone https://github.com/eMahtab/node-express-hello-world
  cd node-express-hello-world
  npm install
  npm start

  Go to localhost:4000

```  
# Prerequisites : 
## Running kubernetes cluster 
make sure you have running kubernetes cluster on cloud or on hosted locally (kind - minikube ..etc)
## Install liknkerd 
https://www.digitalocean.com/community/tutorials/how-to-install-and-use-linkerd-with-kubernetes 
## Install Linkerd-SMI extension for canary deployment 
https://linkerd.io/2.15/tasks/linkerd-smi/#install-the-linkerd-smi-extension   

# Usage : 

```
   kubectl create ns <ns-name>
   kubectl annotate ns <ns-name> linkerd.io/inject=enabled
   cd node-express-hello-world/k8s 
   kubectl apply -f version-I -n <ns-name>
   kubectl apply -f version-II -n <ns-name>
   kubectl apply -f traffic-split.yaml -n <ns-name>

```

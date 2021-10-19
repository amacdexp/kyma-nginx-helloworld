# kyma-nginx-helloworld


Example helloworld running on SAP Kyma, using nginx demo image  

[NGINX webserver that serves a simple page](https://github.com/nginxinc/NGINX-Demos/tree/master/nginx-hello)

Can be run on a SAP Kyma trial (a Kubernetes [k8s] service)

[SAP Kyma runtime available in trial] (https://blogs.sap.com/2020/10/09/kyma-runtime-available-in-trial-and-now-we-are-complete/)

# Steps
```
#Download kubeconfig.yml from Kyma console.. See download/export option under 'User Profile' - top right corner

## windows cmd
>> Set KUBECONFIG=C:\Users\<user>\Downloads\kubeconfig.yml 
## windows powershell
>> $env:KUBECONFIG="C:\Users\<user>\Downloads\kubeconfig.yml" 
## linux
>> export KUBECONFIG=/Users/<user>/Downloads/kubeconfig.yml 


#Create a namespace... e.g. dev

#Check the cluster in your new namespace
kubectl cluster-info  -n dev

#Deploy image
kubectl replace --force -n dev -f deployment.yaml  
```

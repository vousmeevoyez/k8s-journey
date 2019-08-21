# PODS
pod is smallest unit of deployment in kubernetes, it represent collection of containers sharing a network and mount namespace.

#  Commands related to PODS usage

## launch a pod using some docker image
`kubectl run deployment_name --image=image_going_to_deployed --port=port_going_to_be_exposed`
example: `kubectl run sise --image=mhausenblas/simpleservice:0.5.0 --port=9876`

## check all running pods
`kubectl get pods` 

## launch a pod using configuration file
`kubectl apply -f some_deployment.yaml`

## access running container inside pod
`kubectl exec pod_name -c container_name`

## get more information about pod
`kubectl describe pod_name`

## remove running pod
`kubectl delete pod pod_name`

### Notes
launching one or more containers (together) in Kubernetes is simple, however doing it directly comes with serious limitation, you have to manually take care the running cycle in case of failure.

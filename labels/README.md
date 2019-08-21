## Labels
Label are mechanism you use to organize kubernetes objects. Label is a key value pair with certain restrictions concerning length and allowed values but without any predefined meaning.

## How to add
there are 2 ways to add label on a pods:
1. define it inside the yaml
2. use k8s command ` kubectl label pods pod_name key=value `

## Filter pod by labels
`kubectl get pods --selector key=value`
		or
`kubectl get pods -l key=value`

## multiple filter
`kubectl get pods -l 'key in (value1, value2)'`

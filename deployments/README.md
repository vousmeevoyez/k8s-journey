## DEPLOYMENTS
deploment is supervisor for pods, giving fine grained control over how and when an new pod version is rolled out as well as rolled back to a previous state
deployment consist of -> pod + replica set

### check deployment
`kubectl rollout status deploy/deployment_name`

### deployment history
`kubectl rollout history deploy/deployment_name`

### undo deployment
`kubectl rollout undo deploy/deployment_name --to-revision=revision_no`

# How to Integrate K8s to Gitlab

## Quick Start

We need to get generated k8s credentials connected into gitlab

+ kubectl get secrets
+ after getting all secrets stored on cluster we choose default or ingress token and get its service token
  - kubectl -o json get secrets secret-name | jq -r '.data.token' | base64 -d
    * Copy this to gitlab
  - kubectl -o json get secrets secret-name | jq -r '.data."ca.crt"' | base64 -d - | tee ca.crt
    * Copy this to gitlab 

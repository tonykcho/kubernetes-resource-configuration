# Install

(https://www.elastic.co/guide/en/cloud-on-k8s/current/k8s-deploy-eck.html)

# Get credentials

```
PASSWORD=$(kubectl get secret quickstart-es-elastic-user -o go-template='{{.data.elastic | base64decode}}')

kubectl get secret quickstart-es-elastic-user -o go-template='{{.data.elastic | base64decode}}'
```

## Kibana
```
kubectl get secret quickstart-es-elastic-user -o=jsonpath='{.data.elastic}' | base64 --decode; echo
```
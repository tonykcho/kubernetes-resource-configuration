# Common used command

# Configmap
Create configmap

```
kubectl create configmap config --from-file <file1>
```

Apply configmap and inject file.
```
volumeMounts:
- name: "config"
    mountPath: "/<existing folder>/<file1>"
    subPath: "<file1>"
- name: "config"
    mountPath: "/<existing folder>/<file2>"
    subPath: "<file2>"
volumes:
- name: "config"
    configMap:
    name: "config"
```

# Restart deployment

```
kubectl rollout restart deployment/<deployment>
```
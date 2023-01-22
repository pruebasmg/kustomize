- Pregunta

Create an inline json6902 patch in the kustomization.yaml file to remove the label org: kodekloud from the mongo-deployment.


```
patches:
  - target:
      kind: Deployment
      name: mongo-deployment
    patch: |-
      - op: remove
        path: /spec/template/metadata/labels/org
```

y correr

kubectl apply -f /root/code/k8s

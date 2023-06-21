# Overview

Run the following commands to generate the pod definitions with the different ENV variables:

```bash
kubectl kustomize prod > pod-prod.yaml
kubectl kustomize dev > pod-dev.yaml
```

You can see the differences between these two files using diff`.

```bash
diff pod-dev.yaml pod-prod.yaml

9c9
<       value: postgres://dev:5432
---
>       value: postgres://prod:5432
```

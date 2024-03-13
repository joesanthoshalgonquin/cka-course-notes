# Section 2
## Commands
- kubectl create -f file_name.yaml = Create a pod from yaml file
- kubectl get pods = Get the number of pods
- kubectl describe pod pod_name = Show description of the POD

## Create a POD using YAML
- metadata fields have to be indented at same level
- labels can have any key-value pairs while metada there are specific properties
- additional info about object
- containers is a list or array because a pod can have multiple containers
- The - represents the index of the list, i.e. the nginx-container is the first one in the list below

```
apiVersion: v1
kind: Pod
metadata:
  name: myapp-pod
  labels:
    app: myapp
    type: front-end
spec:
  containers:
    - name: nginx-container
      image: nginx
```
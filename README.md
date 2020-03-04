# Boinc for Docker
An up to date version of Boinc for Docker including a kubernetes file

# Usage
```
docker run --name=boinc -d techwolf12/boinc:stable \
  -attach_project boinc.bakerlab.org/rosetta/ \
                  <YOUR boinc.bakerlab.org ACCOUNT KEY>
```

# Kubernetes
Kubernetes can be used as such (do add your key to the boinc.yaml file first):

```
kubectl create namespace boinc
kubectl -n boinc apply -f boinc.yaml
```
To scale it up/down:
```
kubectl -n boinc scale rc boinc-workers --replicas=2
```
And to remove it:
```
kubectl -n boinc delete -f boinc.yaml
```

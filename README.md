#Boinc for Docker
An up to date version of Boinc for Docker including a kubernetes file

```
docker run --name=boinc -d techwolf12/boinc:stable \
  -attach_project boinc.bakerlab.org/rosetta/ \
                  <YOUR boinc.bakerlab.org ACCOUNT KEY>
```

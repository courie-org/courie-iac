# courie-iac
This repository was originally responsible for containing resources for deploying Courie. As more services were created, this repo has turned into cluster prep. Each of the service-specific Helm charts have been moved to the code's repository. 

For now, this is just OCP templates to be applied in order to prepare the cluster. 

## Cluster Prep
In the cluster-setup directory, run each resource bundle in order. Please note, you will need to wait after "1-operator-install.yaml" is done installing before preceding. 

```
oc apply -f 0-projects.yaml
oc apply -f 1-operator-install.yaml
oc apply -f 2-service-mesh.yaml
oc apply -f 3-amq-streams.yaml
oc apply -f 4-redis.yaml
```
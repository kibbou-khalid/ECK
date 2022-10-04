# Getting Started With ECK on OpenShift on IBM Cloud

### Login to IBM cloud with the generated Passcode 
```
ibmcloud login -sso
```

### Login to the cluster

Generate a new [Passcode](https://iam.cloud.ibm.com/identity/passcode).

Authenticate to the cluster using the generated Passcode
```
oc login -u passcode -p {passwocode} --server=https://c104-e.private.ca-tor.containers.cloud.ibm.com:32438
```

### login to kibana
oc get secret elasticsearch-es-elastic-user -o go-template='{{.data.elastic | base64decode}}'

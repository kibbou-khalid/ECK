# Getting Started With ECK on OpenShift

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

## Documentation used to deploy ECK on Openshift

### Deploy elasticsearch, Kibana and metricbeat
https://www.elastic.co/guide/en/cloud-on-k8s/current/k8s-openshift-deploy-elasticsearch.html
https://cloud.redhat.com/blog/run-elastic-cloud-on-kubernetes-on-red-hat-openshift

### Deploy heartbeat, filebeat
https://www.elastic.co/guide/en/cloud-on-k8s/current/k8s-openshift-beats.html

### login to kibana
oc get secret elasticsearch-es-elastic-user -o go-template='{{.data.elastic | base64decode}}'

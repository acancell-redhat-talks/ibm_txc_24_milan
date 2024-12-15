### Check Cluster and Nodes status 

1. Access the OpenShift console at `https://console-openshift-console.apps.HOSTNAME/dashboards`
2. Go to _Home_ > _Overview_ and check `Cluster ID` and `OpenShift version`
3. Go to _Compute_ > _Nodes_, then select a node, then:
    - go to _Overview_ and check the Node base metrics
    - go to _Details_ and check the Node CPU `Architecture` 

### Check Cluster observability

1. Go to _Observe_ > _Dashboard_ and check `API Performance` and `etcd` dashboards
2. Go to _Observe_ > _Alerting_ and check currently active alerts

### Check the API objects within `demo-project` 

1. Go to _Workloads_ > _Pods_
2. Select Project `demo-project`
3. Select Pod `demo-pod`
4. Check each of the following tabs: `Details`, `Metrics`, `YAML`, `Logs`, `Terminal`
5. Go to _Networking_ > _Services_
6. Select Service `demo-service`
7. Check each of the following tabs: `YAML`, `Pods`

### Review an example of microservices-based application

1. _NOTE_ The deployed application source code can be found on https://github.com/acancell-redhat/onlineboutique-micro-ppc64le
2. In the OpenShift console switch to project `onlineboutique-micro-ppc64le`
3. Click on tab `Administrator` and switch to `Developer`
4. Review the application `Topology`
5. Go to `frontend` and click on _Open URL_
6. Go to `frontend` > _Edit Pod count_ and move from `2` to `3`, then wait for the scaling to complete
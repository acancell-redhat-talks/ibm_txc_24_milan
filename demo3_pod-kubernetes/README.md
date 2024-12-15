### Create a Pod definition from a container

1. Go to _Podman Desktop_ > _Containers_ 
2. Select tab _All_
3. Select the container `demo-container`
4. Go to _Action_ > _Deploy to Kubernetes_
5. Set the following parameters:
    - _Pod Name_: `demo-pod`
6. Review the generated YAML file

### Deploy the Pod on a Kubernetes cluster

1. From the same window of previous paragraph, set the following parameters:
    - _Kubernetes Context_: (the desired Kubernetes cluster, in the format `PROJECT/api-HOSTNAME:6443/USER`)
    - _Kubernetes Namespace_: (the desired Kubernetes namespace, for example `demo-project`)
2. Click on _Deploy_
3. After the Pod is reported as _running_, click on _Done_

### Check the Pod status

1. Go to _Podman Desktop_ > _Pods_ 
2. Select tab _Running_
3. Select the desired pod
4. Select tab _Summary_
5. Check _Details_ > _Node Name_ to verify on which node the Pod is running	

### Check other Kubernetes resources

1. Go to _Podman Desktop_ > _Kubernetes_ > _Nodes_
2. Check the Nodes list
3. Go to _Podman Desktop_ > _Kubernetes_ > _Ingresses and Routers_
4. Select the desired Ingress / Router and open its related _HOST/PATH_
5. NOTE The _HOST/PATH_ might be exposed with a self-signed certificate, therefore it might trigger an alert in the web browser
Remove taint from nodes

`kubectl taint nodes --all node-role.kubernetes.io/master-`


Set node lable


`kubectl label nodes knode1 name=knode1`


Show all nodes with labels

`kubectl get nodes --show-labels`


Auto inject sidecar to the default namepsace 

`kubectl label namespace default istio-injection=enabled`


Disable auto sidecar injection for the default namespace

`kubectl label namespace default istio-injection=disabled --overwrite`


Get Istio auto injection status

`kubectl get namespace -L istio-injection`


Path external ip to service

`kubectl patch -n <namespace> svc <service-name> -p '{"spec":{"externalIPs":["192.168.0.5"]}}'`


Create config map containing folder contents

`kubectl create configmap <name> --from-file=<folder/path>`

`kubectl describe configmaps <name>`

`kubectl get configmaps <name> -o yaml`



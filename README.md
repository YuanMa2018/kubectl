# kubectl
This is a folder contains some kubectl script that is for easy pull container from INKO(UDE).

# get status of runing pods and deployment
kubectl get pods,deployment

# delete pods/deployment
kubectl delete pod/deployment $name_pod/deployment

# access in a container
kubectl exec -it $name_pod bash

# Starting a new container by configura file
kubectl apply -f */kubectl/container_config/py3-tf1.3-yuanma-3d-object-detection.yaml

# Startinf a new pvc(Persistent Volume Claim) by configura file
kubectl apply -f */kubctl/storage_config/pvc-yuanma-3d-object-detection.yaml

# create a service which expose deployment's target-port(8000) to container's virtual ip's port(80), this virtual ip can not be access in outside, but in kubenetes networks. 
kubectl expose deployment d1 --port=80 --target-port=8000 --type=NodePort

# project localhost:8888 to kubenetes's node (have deployment d1) virtual ip:80
kubectl port-forward --address localhost d1-xxx 8888:80

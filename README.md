# kubectl
This is a folder contains some kubectl script that is for easy pull container from INKO(UDE).

# get status of runing pods and deployment
kubectl get pods,deployment

# access in a container
kubectl exec -it "" bash

# Starting a new container by configura file
kubectl apply -f */kubectl/container_config/py3-tf1.3-yuanma-3d-object-detection.yaml

# Startinf a new pvc(Persistent Volume Claim) by configura file
kubectl apply -f */kubctl/storage_config/pvc-yuanma-3d-object-detection.yaml


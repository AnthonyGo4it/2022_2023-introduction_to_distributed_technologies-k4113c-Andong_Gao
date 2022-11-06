University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies)
Year: 2022/2023
Group: K4113c
Author: Gao, Andong
Lab: Lab4
Date of create: 05.11.2022
Date of finished: 06.11.2022





Start CNI calico with Multi-node Cluster (2 node): minikube start --network-plugin=cni --cni=calico

Adding an worker node: minikube node add
Check calico working: kubectl get pods -l k8s-app=calico-node -A 
Label 2 nodes with zone-label: kubectl label nodes minikube zone=west and kubectl label nodes minikube-02 zone=east
Create ippool with 2 labels in step 4: kubectl apply -f ip.yaml
Create deployment with 2 replicaset and env: kubectl apply -f replicaset.yaml
Ceate service for deployment: kubectl apply -f svc.yaml
Forward it to port. Result in Pic 2: kubectl port-forward service/web-service 3000:3000

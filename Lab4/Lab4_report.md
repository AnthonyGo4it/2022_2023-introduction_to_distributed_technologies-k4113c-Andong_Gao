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
![Image text](https://github.com/AnthonyGo4it/2022_2023-introduction_to_distributed_technologies-k4113c-Andong_Gao/blob/main/Lab4/Screen%20Shot%202022-11-07%20at%2001.42.31.png)


Adding an worker node: minikube node add
![Image text](https://github.com/AnthonyGo4it/2022_2023-introduction_to_distributed_technologies-k4113c-Andong_Gao/blob/main/Lab4/Screen%20Shot%202022-11-07%20at%2001.44.11.png)

Check calico working: kubectl get pods -l k8s-app=calico-node -A 
![Image text](https://github.com/AnthonyGo4it/2022_2023-introduction_to_distributed_technologies-k4113c-Andong_Gao/blob/main/Lab4/Screen%20Shot%202022-11-07%20at%2001.44.38.png)


Label 2 nodes with zone-label: kubectl label nodes minikube zone=west and kubectl label nodes minikube-m02 zone=east
![Image text](https://github.com/AnthonyGo4it/2022_2023-introduction_to_distributed_technologies-k4113c-Andong_Gao/blob/main/Lab4/Screen%20Shot%202022-11-07%20at%2001.44.52.png)


Create ippool with 2 labels in step 4: kubectl apply -f ip.yaml
Create deployment with 2 replicaset and env: kubectl apply -f replicaset.yaml
Ceate service for deployment: kubectl apply -f svc.yaml

Forward it to port. Result in Pic 2: kubectl port-forward service/web-service 3000:3000
![Image text](https://github.com/AnthonyGo4it/2022_2023-introduction_to_distributed_technologies-k4113c-Andong_Gao/blob/main/Lab4/Screen%20Shot%202022-11-07%20at%2001.45.34.png)

Ping check from this pod to that pod using kubectl exec: kubectl exec -it webserver -- ping 10.244.102.2
Successfully ping from pod to other pod


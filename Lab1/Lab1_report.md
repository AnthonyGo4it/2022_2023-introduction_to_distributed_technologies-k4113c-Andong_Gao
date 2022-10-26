University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies)
Year: 2022/2023
Group: K4113c
Author: Gao, Andong
Lab: Lab1
Date of create: 20.09.2022
Date of finished: 21.10.2022


Answers of questions:
1. Process
minikube start: Starting minikube
kubectl apply -f mymanifest.yaml: Applying the configuration of manifest to create pod
![Image text](https://github.com/AnthonyGo4it/2022_2023-introduction_to_distributed_technologies-k4113c-Andong_Gao/blob/main/Lab1/Screen%20Shot%202022-10-21%20at%2001.35.41.png)

![Image text](https://github.com/AnthonyGo4it/2022_2023-introduction_to_distributed_technologies-k4113c-Andong_Gao/blob/main/Lab1/Screen%20Shot%202022-10-21%20at%2001.36.15.png)

kubectl get pods (Optional): List all pods that minikube has

minikube kubectl -- expose pod vault --type=NodePort --port=8200: Exposing to create new service NodePort type with port 8200
![Image text](https://github.com/AnthonyGo4it/2022_2023-introduction_to_distributed_technologies-k4113c-Andong_Gao/blob/main/Lab1/Screen%20Shot%202022-10-21%20at%2001.36.37.png)

kubectl port-forward service/vault 8200:8200: Getting to container on port 8200
![Image text](https://github.com/AnthonyGo4it/2022_2023-introduction_to_distributed_technologies-k4113c-Andong_Gao/blob/main/Lab1/Screen%20Shot%202022-10-21%20at%2001.36.49.png)

minikube stop: Stopping minikube

we access to the vault web
![Image text](https://github.com/AnthonyGo4it/2022_2023-introduction_to_distributed_technologies-k4113c-Andong_Gao/blob/main/Lab1/Screen%20Shot%202022-10-21%20at%2001.37.09.png)





2. Where can I get a token to enter the Vault? ( Hint: Logs are the head of everything )
Using command "kubectl logs vault" then find root token in logs.
-docker logs d6f17b361ead
![image](https://user-images.githubusercontent.com/115359561/197932192-1a5f3514-74aa-4377-94f1-24dba7c045bd.png)


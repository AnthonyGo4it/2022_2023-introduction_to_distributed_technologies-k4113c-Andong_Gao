University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies)
Year: 2022/2023
Group: K4113c
Author: Gao, Andong
Lab: Lab1
Date of create: 20.09.2022
Date of finished: 31.09.2022

Answers of questions:

Что сейчас произошло и что сделали команды указанные ранее?
We can access to vault via link: http://localhost:8200
minikube start: Starting minikube
kubectl apply -f C:\Users\TrungNM\Desktop\desk\introduction\mymanifest.yaml: Applying the configuration of manifest to create pod
kubectl get pods (Optional): List all pods that minikube has
minikube kubectl -- expose pod vault --type=NodePort --port=8200: Exposing to create new service NodePort type with port 8200
kubectl port-forward service/vault 8200:8200: Getting to container on port 8200
minikube stop: Stopping minikube
Где взять токен для входа в Vault?
Using command "kubectl logs vault" then find root token in logs.

schema_lab1 drawio
Schema 1 - Nodeport working

Capture Picture 1 - Loggin page using token on vault

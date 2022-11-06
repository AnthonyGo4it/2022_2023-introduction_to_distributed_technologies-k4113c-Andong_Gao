University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies)
Year: 2022/2023
Group: K4113c
Author: Gao, Andong
Lab: Lab1
Date of create: 05.11.2022
Date of finished: 06.11.2022


minikube start: 
![Image text](https://github.com/AnthonyGo4it/2022_2023-introduction_to_distributed_technologies-k4113c-Andong_Gao/blob/main/Lab3/Screen%20Shot%202022-11-07%20at%2000.08.46.png)

Create and apply replicaset and define the environment with value from configmap, created the svc,ingress,cm: 
![Image text](https://github.com/AnthonyGo4it/2022_2023-introduction_to_distributed_technologies-k4113c-Andong_Gao/blob/main/Lab3/Screen%20Shot%202022-11-07%20at%2000.09.12.png)

brew install mkcert for fqdn host:
![Image text](https://github.com/AnthonyGo4it/2022_2023-introduction_to_distributed_technologies-k4113c-Andong_Gao/blob/main/Lab3/Screen%20Shot%202022-11-07%20at%2000.10.04.png)

Host ini: define the host that we could access via after deploy. Here: lab3.example.com
![Image text](https://github.com/AnthonyGo4it/2022_2023-introduction_to_distributed_technologies-k4113c-Andong_Gao/blob/main/Lab3/Screen%20Shot%202022-11-07%20at%2000.14.24.png)

Create secret with certificate and private key: 
![Image text](https://github.com/AnthonyGo4it/2022_2023-introduction_to_distributed_technologies-k4113c-Andong_Gao/blob/main/Lab3/Screen%20Shot%202022-11-07%20at%2000.14.41.png)

Run: minikube tunnel, results showing: 
![Image text](https://github.com/AnthonyGo4it/2022_2023-introduction_to_distributed_technologies-k4113c-Andong_Gao/blob/main/Lab3/Screen%20Shot%202022-11-07%20at%2000.20.41.png)

How Ingress works with TLS:
![Image text](https://github.com/AnthonyGo4it/2022_2023-introduction_to_distributed_technologies-k4113c-Andong_Gao/blob/main/Lab3/Screen%20Shot%202022-11-07%20at%2000.15.44.png)


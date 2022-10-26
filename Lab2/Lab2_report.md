University: ITMO University
Faculty: FICT
Course: Introduction to distributed technologies
Year: 2022/2023
Group: K4112c
Author: Nguyen Manh Trung
Lab: Lab2
Date of create: 24.09.2022
Date of finished: 31.09.2022

Creating a deployment with manifest name webserver.yaml.: kubectl apply -f webserver.yaml
In this file, define the environment values with keys: REACT_APP_USERNAME and REACT_APP_COMPANY_NAME. This deployment has 3 replicasets.
Then, creating a service with type NodePortand port is container port in the webserver manifest: kubectl apply -f webserver-svc.yaml

Create a service through which you will have access to these "pods". 
-kubectl get pods
-minikube kubectl -- expose pod webserver-866c8bfbd-929c4 --type=NodePort --port=3000
Start in minikubeport forwarding mode 
-minikube kubectl -- port-forward service/webserver-866c8bfbd-929c4 3000:3000   

After that, we can access to website via localhost port 3000 and values for key that we defined in env appeared:

![Image text](https://github.com/AnthonyGo4it/2022_2023-introduction_to_distributed_technologies-k4113c-Andong_Gao/blob/main/Lab2/Screen%20Shot%202022-10-26%20at%2011.36.55.png)

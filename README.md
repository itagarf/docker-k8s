# docker-k8s

A python web application deployed on dockerhub, then deployed on kubernetes.
To run the k8s commands:
```
% k get deployments
NAME             READY   UP-TO-DATE   AVAILABLE   AGE
home-inspire     1/1     1            1           16d

% k get services
NAME           TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)        AGE
home-inspire   NodePort    10.110.225.138   <none>        80:30003/TCP   16d

% k get pods       
NAME                              READY   STATUS    RESTARTS      AGE
home-inspire-6bf848cfb7-cmfsk     1/1     Running   1 (56s ago)   16d

% minikube service home-inspire #or k port-forward services/home-inspire 8080:80
```

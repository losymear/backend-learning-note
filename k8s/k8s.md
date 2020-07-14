## 概览
Kubernetes是一个开源的，用于管理云平台中多个主机上的容器化的应用，Kubernetes的目标是让部署容器化的应用简单并且高效（powerful）,Kubernetes提供了应用部署，规划，更新，维护的一种机制。

## 构成
[k8s架构](achitecture.png)

### pod
一个服务的最小服务单元，同一个服务可存在多个pod，多个pod之间使用相同的镜像及环境变量。

### deployment
用于管理一个服务的多个pods，可以指定服务部署形式（部署过程种是否先关闭旧服务等）。

### service
用来访问同一个服务的一组pods，实现负载均衡。

### ingress配置
类似ngnix，将请求根据url转发到不同的service。同时指定请求使用的https证书。

### config配置
key-value形式的环境变量配置，pod部署时可以指定使用某一个变量。

### secrets
https证书管理


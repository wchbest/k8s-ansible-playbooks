## metrics-server

[metrics-server](https://github.com/kubernetes-incubator/metrics-server.git)

```
# 镜像准备(换成可下载地址)
k8s.gcr.io/metrics-server-amd64:v0.3.4

# 部署
$ git clone https://github.com/kubernetes-incubator/metrics-server.git
$ cd metrics-server/deploy/
$ kubectl  apply -f 1.8+/

# 查看部署详情

$ kubectl  get all -n kube-system | grep metrics

pod/metrics-server-6f587bb6fb-mpj4b    1/1     Running   0          12m

service/metrics-server            ClusterIP   10.253.88.16    <none>        443/TCP                  26m



deployment.apps/metrics-server   1/1     1            1           26m

replicaset.apps/metrics-server-6f587bb6fb   1         1         1       12m
replicaset.apps/metrics-server-79679855f7   0         0         0       26m

```

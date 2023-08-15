# Resultados

Participantes
- Zinhue Gonzalez MOntelongo
- Jose Miguel Villafuerte Sandoval

Kubercoins-deploy-result
NAME    TYPE       CLUSTER-IP      EXTERNAL-IP   PORT(S)        AGE   SELECTOR
webui   NodePort   10.97.123.242   <none>        80:31981/TCP   12m   app=webui

Kubercoins-liveness-probe-results
kubectl get svc rng
NAME   TYPE        CLUSTER-IP     EXTERNAL-IP   PORT(S)   AGE
rng    ClusterIP   10.105.42.33   <none>        80/TCP    8s

httping 54.187.70.17
PING 54.187.70.17:80 (/):
could not connect (Connection refused)
kubectl get pods -w

NAME                      READY   STATUS    RESTARTS   AGE
hasher-65db859b66-mtgnf   0/1     Pending   0          2m44s
redis-6ff7cd7598-5lzkb    0/1     Pending   0          2m44s
rng-5c9cd7744c-4rrqk      0/1     Pending   0          2m43s
webui-6969bf568c-mffqv    0/1     Pending   0          2m43s
worker-6bbc87d469-q5j88   0/1     Pending   0          2m43s

$ ab -c 10 -n 1000 http://54.187.70.17/1
This is ApacheBench, Version 2.3 <$Revision: 1879490 $>
Copyright 1996 Adam Twiss, Zeus Technology Ltd, http://www.zeustech.net/
Licensed to The Apache Software Foundation, http://www.apache.org/

Benchmarking 54.187.70.17 (be patient)
apr_socket_recv: Connection refused (111)
[54.187.70.17] (kubernetes-admin@kubernetes:yellow) k8s@test1 ~/kubercoins
$ cd ~/kubercoins
kubectl delete -f .
kns default
kubectl delete namespace yellow
deployment.apps "hasher" deleted
service "hasher" deleted
deployment.apps "redis" deleted
service "redis" deleted
deployment.apps "rng" deleted
service "rng" deleted
deployment.apps "webui" deleted
service "webui" deleted
deployment.apps "worker" deleted
Context "kubernetes-admin@kubernetes" modified.
Active namespace is "default".
namespace "yellow" deleted


Kubercoins-test-results

```bash
docker run --rm --net host -v $PWD:/vol \
    -v /etc/kubernetes/pki/etcd:/etc/kubernetes/pki/etcd:ro \
    -e ETCDCTL_API=3 k8s.gcr.io/etcd:3.3.10 \
    etcdctl --endpoints=https://[127.0.0.1]:2379 \
            --cacert=/etc/kubernetes/pki/etcd/ca.crt \
            --cert=/etc/kubernetes/pki/etcd/healthcheck-client.crt \
            --key=/etc/kubernetes/pki/etcd/healthcheck-client.key \
            snapshot save /vol/snapshot
```


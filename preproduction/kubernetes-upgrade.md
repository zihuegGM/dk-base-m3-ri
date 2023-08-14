# Actualización de Kubernetes

Cluster:
preproducción

Actividades:
- [nodo 1/control plane] - Actualizar el control plane de Kubernetes
  - Verificar la versión de kubectl y el API server.
  - Verificar la versión de los nodos.
  - Verificar las versiones del control plane.
  - Descargar la versión correcta de kubeadm.
  - Actualizar el control plane.
- [nodos 1+/worker node, incluye el control plane] - Actualizar los worker nodes de Kubernetes
  - Descargar la versión correcta de kubeadm.
  - Actualizar kubeadm.
  - Instalar kubelet con la versión requerida.
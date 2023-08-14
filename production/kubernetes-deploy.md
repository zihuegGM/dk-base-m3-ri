# Instalación de Kubernetes

Cluster:
producción

Objetivo:
Instalar Kubernetes en el ambiente de producción.

Actividades:
- [nodo 1/control plane] - Instalar Kubernetes en el control plane
  - Copiar los archivos `kubernetes-apt-key.gpg` y `lib/containerd-config.toml`
  - Asignar a KUBEVERSION el valor requerido para la instalación.
  - Ejecutar los comandos para designar esta versión como la preferida.
  - Precargar la llave de Kubernetes.
  - Instalar paquetes.
  - Instalar las herramientas de Kubernetes.
  - Configurar y reiniciar containerd.
  - Crear el archivo kubeadm-config.yaml con los valores requeridos para la instalación.
  - Inicializar el cluster.
  - Añadir kubeconfig a la cuenta del usuario.
  - Instalar la red de pods Weave.
  - Instalar el servidor de métricas.
- [nodo 2+, worker node]
  - Copiar los archivos `kubernetes-apt-key.gpg` y `lib/containerd-config.toml`
  - Asignar a KUBEVERSION el valor requerido para la instalación.
  - Ejecutar los comandos para designar esta versión como la preferida.
  - Precargar la llave de Kubernetes.
  - Instalar paquetes.
  - Instalar las herramientas de Kubernetes.
  - Configurar y reiniciar containerd.
  - Obtener el archivo kubeadmconfig del nodo 1.
  - Ingresar el nodo al cluster.
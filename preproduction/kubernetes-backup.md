# Respaldo de Kubernetes

Cluster:
preproducción

Objetivo:
Respaldar la base llave/valor etcd.

Actividades:
- Crear un respaldo de etcd por medio de la herramienta `etcdctl`, especificando:
  - variable de entorno para `etcdctl v3`.
  - dirección del servidor a respaldar.
  - ruta a la llave, certificado y certificado CA.
- Verificar que se haya creado un archivo llamado snapshot en el directorio donde se invocó el comando.
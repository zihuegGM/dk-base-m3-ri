# Integrar liveness probe a KuberCoins

Cluster:
desarrollo

Objetivo: 
Integrar un liveness probe a la aplicación KuberCoins por medio de un YAML manifest e imágenes preconstruidas. La liveness probe será añadida al DaemonSet de `rng`.

Actividades:
- Crear un namespace para la integración.
- Activar el namespace.
- Obtener los manifests de KuberCoins.
- Añadir el liveness probe al deployment YAML de `rng` con las siguientes especificaciones:
  - verbo: Get
  - path: /
  - puerto: 80
  - delay inicial (segundos): 30
  - periodo (segundos): 5
- Cargar el YAML para todos los recursos de KuberCoins.
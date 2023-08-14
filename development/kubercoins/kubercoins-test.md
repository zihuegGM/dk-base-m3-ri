# Confirmar KuberCoins

Cluster:
desarrollo

Objetivo:
Generar tráfico para confirmar el comportamiento de KuberCoins.

Detalles:
El servicio `rng` requiere de 100ms para procesar una solicitud.
El timeout del probe es de 1 segundo.
Al enviar más de 10 solicitudes por segundo por backend, fallará el probe.

Actividades:
- Monitorear los eventos del cluster.
- Monitorear el tiempo de respuesta de `rng`.
- Monitorear el estatus del pod.
- Generar tráfico con distintas cantidades de solicitudes concurrentes.
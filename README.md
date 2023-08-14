# Docker+Kubernetes - Módulo 3 - Reto Integrador

## Introducción

El equipo de sistemas de Contoso, Inc. se encuentra en proceso de modernización de sus sistemas. Por ello, han decidido integrar las tecnologías de contenedores y orquestación para como soporte a la mejor continua de sus procesos de desarrollo y liberación de aplicaciones.

Contoso, Inc. está desplegando clusters de Kubernetes con el fin de validar aspectos relacionados con la administración y operación de esta tecnología.

## Clusters de Kubernetes

Proveedor: Amazon Web Services

- Entrenamiento: el equipo de Contoso Inc. cuenta con acceso a diversos clusters de Kubernetes modalidad "sandbox" que fueron empleados como parte de un entrenamiento que recibieron en Docker y Kubernetes.
- Desarrollo, 1 nodo control plane incluyendo worker node, Kubernetes v1.27.4.
- Preproducción, 1 nodo control plane más 2 nodos worker node, Kubernetes v1.26.0 instalado.
- Producción, 1 nodo control plane más 2 nodos worker node, Kubernetes no instalado, se requiere v1.27.4.

Los clusters de entrenamiento se encuentran en la región us-west-2 con la Virtual Private Cloud por omisión y reglas personalizadas en el Security Group para admitir diversos flujos inbound requeridos por Kubernetes y las aplicaciones.

Los clusters desarrollo, preproducción y producción se encuentran en la región us-west-1 con la Virtual Private Cloud por omisión y regla personalizada en el Security Group para admitir tráfico inbound de SSH solamente.

Estos clusters fueron desplegados por un asesor del equipo de sistemas quien de momento se encuentra fuera del país.

De momento no se cuenta con una lista formal de los flujos requeridos por los componentes de sistema y las aplicaciones, por lo que se tiene como objetivo documentar los flujos necesarios conforme se completen los trabajos pendientes en cada uno de los clusters.

El equipo tiene el compromiso de completar el despliegue lo antes posible con el fin de generar un reporte que presentarán a sus directores. Esto debe ocurrir al cierre de una reunión de trabajo del día de hoy.

El asesor del equipo de Contoso, Inc. compartió las siguientes notas respecto a las tareas pendientes en los clusters:

## Tareas pendientes

- Desarrollo
  - Instalar KuberCoins.
  - Integrar liveness probe a KuberCoins.
  - Confirmar el liveness probe de KuberCoins

- Preproducción
  - Efectuar respaldo de cluster previo a la adición de nodos e instalación de aplicaciones.
  - Actualizar cluster de Kubernetes a v1.27.4.
  - Instalar KuberCoins con liveness probe integrada.
  - Confirmar acceso a KuberCoins para clientes conectados a Internet.

- Producción
  - Instalar cluster de Kubernetes a v1.27.4.
  - Añadir 2 nodos worker node al cluster.
  - Efectuar respaldo de cluster previo a la instalación de aplicaciones.
  - Instalar KuberCoins con liveness probe integrada.
  - Confirmar acceso a KuberCoins para clientes conectados a Internet.

El detalle de las tareas pendientes se encuentra en su carpeta correspondiente de este repositorio.

## Procedimiento para elaborar las tareas
- Crear un fork de este repositorio.
- Dar seguimiento a las indicaciones en las carpetas de actividades.
- Crear los documentos de respuesta a cada actividad (formato markdown), adjuntar archivos de soporte.

## Entregables
Por cada tarea se requiere un archivo en formato markdown con:
- Actividad realizada.
- Nombre de las personas que participaron en la realización de la actividad.
- Secuencia de comandos empleados (Kubernetes, shell, entre otros).
- Recursos externos requeridos (p.e. flujos de red).
- Artifacto con el resultado de la actividad completada (salida de texto, imagenes).
- El archivo deberá tener el mismo nombre que la tarea con el posfijo `-result.md`. 
  - p.e. la respuesta a `kubercoins-deploy.md` deberá nombrarse `kubercoins-deploy-result.md`.
- La plantilla del archivo de respuesta se encuentra disponible en la carpeta `results/`.

El entregable deberá ser anexado como archivo en la carpeta correspondiente.

# Procedimiento para enviar las tareas
- Efectuar commit y push los archivos de resultados *en el fork que de este repositorio*.
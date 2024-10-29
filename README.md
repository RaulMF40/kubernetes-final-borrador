# Borrador Ejercicio Kubernetes Final
# Despliegue de Frontend y Backend con múltiples versiones en Kubernetes
- Objetivo: Configurar una estructura en Kubernetes para desplegar un frontend y un backend, cada uno con dos versiones. Se deben crear 3 réplicas de cada versión para asegurar alta disponibilidad, o al menos 1 réplica si los recursos del sistema son limitados. Las imágenes utilizadas para el frontend y backend deben ser propias, previamente creadas y subidas a DockerHub en el ejercicio anterior de Docker.

  * Comandos: 
    - minikube start (para iniciar minikube, para que funcione tenemos que tener abierta la aplicacion Docker desktop)
    - minikube addons enable ingress: habilitamos el complemento ingress en minikube para poder gestionar el trafico externo
    - minikube tunnel: Creamos un tunnel (utlizamos Lens para visualizacion con interfaz) para exponer servicios tipo LoadBalancer en Minikube, tal y como tenemos puesto en cada uno de los service. 
    - kubectl apply -f ....deployment.yaml (creamos cada uno de los deployment) 
    - kubectl apply -f ....service.yaml (creamos cada uno de los servicios)
    - kubectl apply -f ingress (creamos la configuracion del ingress para poder gestionar el acceso a los servicios creados anteriormente)
    - kubectl get pods / service / deployment / ingress (nos muestra la información de cada uno)
    - minikube stop (paramos minikue)
    - minikube delete (borramos minikube)


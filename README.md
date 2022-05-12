# ProyectoK8sJA
Microservicios a escala con Docker - Proyecto Final
WordPress App
Deployment Commands:
  kubectl create -f app-configmap.yaml
  kubectl create -f app-secret.yaml
  kubectl create -f fe-persistentvolumeclaim.yaml
  kubectl create -f be-persistentvolumeclaim.yaml
  kubectl create -f fe-service.yaml
  kubectl create -f be-service.yaml
  kubectl create -f fe-deployment.yaml
  kubectl create -f be-deployment.yaml
  kubectl create -f lb-wp.yaml

Deployments estan bajo RollingUpdate con 3 replicas

Rollback Commands:
  kubectl rollout undo
  
Ver histrial del cambio {de acuerdo al yaml por revisar ej abajo fe-deployment:
  kubectl rollout history deploy fe-deployment.yaml

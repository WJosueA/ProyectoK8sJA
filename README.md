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
Para aplicar cambios guardar los cambios en respectivo yaml y ejecutar:{de acuerdo al yaml por revisar ej abajo fe-deployment}
kubectl apply -f fe-deployment.yaml

Rollback Commands:
  kubectl rollout undo
  
Ver historial del cambio {de acuerdo al yaml por revisar ej abajo fe-deployment:
  kubectl rollout history deploy fe-deployment.yaml

View site in localhost currently on port: http://localhost:30935/

## Second components
- *HPA*
- *Ingress*
- *GKE*
- *ConfigMap*
- *Service*
- Job
- Secret


#### Manifiestos


#### liveness 

- comando dentro contenedor 
- peticion tipo http get 
- check tcp port 

#### readiness 
-  revisar que ya esta listo para hacer peticiones
- comando dentro contenedor 
- peticion tipo http get 
- check tcp port 


### HPA  (https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale-walkthrough/)
	- replicas iniciales
	- recursos
	- average use
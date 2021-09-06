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

<a href="https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale-walkthrough/" target="_blank">### HPA</a>

	- replicas iniciales
	- recursos
	- average use
	
### Ingress

proxy pass  a otros servicios

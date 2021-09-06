## Firsts components 
- Docker 
- Deployment
- Replica Set
- Pods
- Kubectl run nginx


### Security 
- Source code
- Version control
- Developer identity
- Diferent account to manage security
- File sshd for docker image


#### Metatron
#### Gandalf authorization


### Kubernetes 

- Automatize 
	-- Build 
		-- code repo (git)
		-- dockerize (jenkins, codebuild)
		-- container image repo (ECR)
	-- Deploy
		-- deploy  (jenkins, codebuild)
		-- kubernetes cluster (EKS)
- Secure 
	- App security
		- POD, namespace, node
		- RBAC (Role-Based Access Control)
		- IRSA (Roles for Service Accounts)
		- 
	- DevOps
		- Authorization
		- Scan repository (Falcon, AWS)
- Cost performance
	- Control Panel 
	- Worker nodes number types
		- Pod resources
		- Unused CPU/memory
	- Get metrics server data
		- CloudWatch container insights
		- Kubecost
		- Cloudhealth
		- Kubernetes resource report
- Version upgrade
	- Rehydarte AMI 
	- Keep aplication running
	- High availability 
	- Maintain pod Disruption budget 
	- Node group
		- AMI 
		- EKS
- Scale 
	- HPA (Horizontal Pod Autoscaler)
	- Cluster autoscaler
	- Cluster Overprovisioning
- Expose service
	- Go over services
		- nodeport 
		- loadbalancer
		- clusterIP 
	- Ingress
		- One load balancer 
			- traefic
			- nginx
			- ALB ingress controller

- Kubernetes for containerized app? 
	- ECS
	- Docker swarm
	- Apache mesos

### Kubernetes best practices

- namespace
	- fisical cluster 
	- naming 
	- Fisical separation
	-   
- resource limit
 	- resources
- Readines liveness probess
	- Readiness (warmup - check ready)
	- Liveness (Pod response for CPU limit)
- security
- Day 2 operations
	- Controls
	- Lifecycle 
		- rolling updates
		- app termination graceful 
	- Incident Response 
		- Idetify isolate
		- PenTesting 



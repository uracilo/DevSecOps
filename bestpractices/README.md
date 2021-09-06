## Flow in DEVOPS


Developer -> Git -> Build -> Integreate -> Staging -> Production -> Monitoring

_________
### Developer
- Pre-commit hook IDE plugins
  - Secure ssh keys, access keys, token etc
  - Filter sensitive data with regex

### Git
- secrets management 
  - Secure config files
  - Tokenize information

### Build
#### Pre- Build 
- Source Composition Analysis SCA
  - We built on frameworks 
  - Third part libraries is the biggest portion of software
  - Identity of 3er part libraries
  
- Static Aplication Security Testing SAST 
  - White box security testing
  - Protect for SQL injection, Cross Site Scripting, Insecure libraries etc 
  - Tool with generic setting so needs manual manage of false-positives 
- Infrastructure as Code 
  - Document version control the infra
  - Audit the infra 
  - Enviroment is a secure as the base image
  - Base image need to be minimal in nature and need to be assessed
- Compliance as code
  - PCI DSS HIPAA SOX
  - 

#### Post- Build 
- Dynamic Aplication Security Testing DAST

### Integreate
- Build Artifacts version agasinst code commit 


### Staging 
- Manual web aplication pentesting business logic flaws

### Production

### Monitoring
- Security in IAAC compliance as code alerting and monitoring what to improve 
  - 

_________






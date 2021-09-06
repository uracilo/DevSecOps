# Docker Security tips 
## base exercice

```docker
# Base Image
FROM node:12-slim
WORKDIR /usr/src/app

# Install Dependencies
COPY package*.json ./
RUN npm install

# Copy in Application
COPY . .

# Run Server
CMD [ "server.js" ]
```



## 1 Dont use Root

```docker
# Base Image
FROM node:12-slim
WORKDIR /usr/src/app

# Install Dependencies
COPY package*.json ./
RUN npm install

# Copy in Application
COPY . .

# ------> Set User to Non-Root
USER node

# Run Server
CMD [ "server.js" ]
```





## 2 Distro less

```docker
###################
### First Stage ###
###################

# Base Image
FROM node:12-slim as build
WORKDIR /usr/src/app

# Install Dependencies
COPY package*.json ./
RUN npm install

# Copy in Application
COPY . .


####################
### Second Stage ###
####################

FROM gcr.io/distroless/nodejs:12

# Copy App + Dependencies from Build Stage

COPY --from=build /usr/src/app /usr/src/app
WORKDIR /usr/src/app

# Set User to Non-Root
USER 1000

# Run Server
CMD [ "server.js" ]
```

## 3 Optimize OS 

- Apparmor
- NSA Security Enhanced Linux
	- Add layers as 
		- Permieter
		- Network
		- Host
		- Aplication
		- Data


## 4 Image scanner

- Ancore
- Clair 
- Google or AWS 


## 5  If you don't know what does id to dont do it. 



_____________________
#### Makefile

```bash
run:
	docker run -i -d -p 8080:8080 node-distroless 

build-naive:
	docker build \
	-f $(CURDIR)/Dockerfile.naive \
	-t node-naive \
	.

build-non-root:
	docker build \
	-f $(CURDIR)/Dockerfile.non-root \
	-t node-non-root \
	.

build-distroless:
	docker build \
	-f $(CURDIR)/Dockerfile.distroless \
	-t node-distroless \
	.
```
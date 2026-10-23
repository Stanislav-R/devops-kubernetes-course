### Evironment: Mac OS + go + colima + minikube

#### Coding stage
Adding svg file, index html and main.go

#### Build stage
go build -o bin/app src/main.go

#### Delivery stage
- Create docker file
- Generate dependencies file
-- go mod init demo
-- colima start
-- docker build .
-- run -p 8080:8080 your-image
-- docker tag your-image your-dockerhub/app:v1.0.0
-- docker login
-- docker push your-dockerhub/app:v1.0.0
-- minikube start
-- kubectl create deploy demo --image your-dockerhub/app:v1.0.0
-- kubectl port-forward deploy/demo 8080



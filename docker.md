### install Docker commands

```
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```

```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
### pull command
```
sudo docker pull <image name>
```

### run command 
```
sudo docker run -d --name jenkins -p 8080:8080 jenkins/jenkins
```
```
sudo docker run -p 3000:3000 -v "$(pwd):/app" -v /app/node_modules geeksdirectory
```
### publish docker image to dockerhub
```
# Step 1: Log in to Docker Hub
docker login

# Step 2: Tag the Docker image
docker tag my-vite-app yourusername/my-vite-app:latest

# Step 3: Push the Docker image to Docker Hub
docker push yourusername/my-vite-app:latest

```

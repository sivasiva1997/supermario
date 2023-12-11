# supermario

🚀 Exciting AWS Tutorial: Deploying Super Mario Game in Docker Container on EC2! 🎮
 
👋 Hey DevOps enthusiasts! Ready for some magic? In this tutorial, I'll guide you through deploying a Super Mario game in a Docker container on an AWS EC2 instance. Shoutout to kaminskypavel for the awesome Docker image on Docker Hub! 🙌
 
💻 Let's get started:
 
1️⃣ First, fire up your EC2 instance (mine's Ubuntu 22.04).
 
 
2️⃣ Update packages to ensure everything is fresh.
apt update
 
 
3️⃣ Install Docker – the heart of our operation.

apt install apt-transport-https ca-certificates curl software-properties-common -y

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

apt update

apt-cache policy docker-ce

apt install docker-ce -y

systemctl status docker
 
 
4️⃣ Docker installation complete! 🎉 Now, onto the fun part!
 
5️⃣ Pull the Super Mario Docker image from Docker Hub.
```
docker pull kaminskypavel/mario
```
  
6️⃣ Verify that the image is in your arsenal.
```
docker images
 
--- 
7️⃣ Run the container and expose it on port 80.

docker run -it -p 80:8080 kaminskypavel/mario

8️⃣ Your container is live! 🚢 Now, grab the public IP, open your browser, and let's play some Mario!
  
🍰 Docker installation is a piece of cake, and now you've got a Super Mario game running on your AWS EC2 instance. 
#DevOps #AWS #Docker #SuperMario #CloudGaming #TechMagic ✨

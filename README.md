# emart-app

# Step by Step Approach 
Use Vagrant for Running a Vagrant VM

Install docker on the vm

# Bring up  containers from docker-compose file
vim docker-compose.yaml  

docker compose up -d

docker compose ps

docker ps -a

ip addr show

# Go to browser enter http://VMIp:80

# Clean up
docker compose down

docker system prune -a

exit (logout out of the Vagrant VM)

vagrant halt


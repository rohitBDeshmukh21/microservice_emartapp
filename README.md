# emart-app

This repository contains the necessary setup to run the `emart-app` using Vagrant for managing the virtual machine and Docker for containerization.

## Step-by-Step Approach

### 1. Use Vagrant for Running a Virtual Machine

Ensure Vagrant is installed on your system. If not, follow the official installation guide for your operating system: [Vagrant Installation Guide](https://www.vagrantup.com/docs/installation)

```bash
# Navigate to the project directory
cd emart-app

# Initialize the Vagrant environment
vagrant up
```

### 2. Install Docker on the VM

SSH into the Vagrant VM and install Docker.

```bash
# SSH into the Vagrant VM
vagrant ssh

# Install Docker (assuming a Debian-based distribution)
sudo apt-get update
sudo apt-get install docker.io
```

### 3. Bring up Containers from Docker Compose File

Edit the `docker-compose.yaml` file if necessary.

```bash
# Navigate to the project directory
cd /vagrant

# Bring up containers using Docker Compose
sudo docker-compose up -d
```

### 4. Verify Container Status

```bash
# Check the status of containers
sudo docker-compose ps

# Or check all containers (including stopped ones)
sudo docker ps -a
```

### 5. Access Application

Open a web browser and enter `http://VMIp:80` where `VMIp` is the IP address of your Vagrant VM.

### 6. Clean Up

```bash
# Stop and remove containers
sudo docker-compose down

# Prune unused Docker resources
sudo docker system prune -a

# Exit from the Vagrant VM
exit
```

### 7. Shutdown Vagrant VM

```bash
# Halt the Vagrant VM
vagrant halt
```

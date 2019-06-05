# GatewayProject

This project consists of several APIs (Application programming interfaces) which provide a secure login, with email verification, to a dashboard where projects may be accessed.

![alt text](https://raw.githubusercontent.com/SamVivers/images/master/MicroservicesSchema.jpg)
where the arrow indicate dirrection of dependance (i.e. mongo-service depends on mongo)

Each API has a Dockerfile allowing docker-compose to deploy the services.

# Setup

clone this dirrectory
  ###### git clone https://github.com/SamVivers/GatewayProject.git

install Docker
  ###### curl https://get.docker.com | sudo bash

and give your user permissions
  ###### sudo usermod -aG docker $(whoami)
  
install docker-compose
  ###### sudo curl -L "https://github.com/docker/compose/releases/download/1.23.2/docker-compose-$(uname -s) -$(uname -m)" -o /usr/local/bin/docker-compose

and give permissions
  ###### sudo chmod +x /usr/local/bin/docker-compose

alter the IP environment variable to match your IP address
  ###### export IP="your IP" (or you can edit the .env file in this repo)

run the .yaml (make sure you are in the GatewayProject directory)
  ###### docker-compose up -d
  
in a browser head to http://"your IP"/authentication/register and sign up
activate your account via the auto-sent email
head to http://"your IP"/authentication/login and login

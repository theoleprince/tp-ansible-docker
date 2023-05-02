# Pull the minimal Ubuntu image
FROM ubuntu:20.04

# Install Nginx
RUN apt-get -y update && apt-get -y install nginx && apt-get install nano sudo -y && apt-get install curl sudo -y && apt-get install software-properties-common sudo -y && apt-add-repository --yes --update ppa:ansible/ansible sudo -y && apt install python3-pip sudo -y

# Expose the port for access
EXPOSE 80/tcp

# Run the Nginx server
CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
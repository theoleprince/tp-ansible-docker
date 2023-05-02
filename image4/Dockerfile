# Pull the minimal Ubuntu image
FROM ubuntu:20.04

# Install Nginx
RUN apt-get -y update && apt-get -y install nginx && apt-get install nano sudo -y && apt-get install curl sudo -y
# RUN  apt-get install letsencrypt sudo -y
# RUN  letsencrypt certonly --standalone --agree-tos --email theophane@gmail.com -d desktop-n7lt95t -d www.desktop-n7lt95t.com --standalone-supported-challenges http-01

# Copy the Nginx config
COPY 01-desktop-n7lt95t.conf /etc/nginx/sites-available/01-desktop-n7lt95t.conf

RUN cd /etc/nginx/sites-enabled  && rm -r default

RUN cd /etc/nginx/sites-enabled && ln -s ../sites-available/01-desktop-n7lt95t.conf

# Expose the port for access
EXPOSE 80/tcp

RUN cd /etc/nginx/sites-available && rm -r default
# Run the Nginx server
CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
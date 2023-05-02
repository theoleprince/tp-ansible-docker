# image ubuntu version 20.04
FROM ubuntu:20.04
# LABEL about the custom image
LABEL maintainer="admin@theo.com"
LABEL version="0.1"
LABEL description="This is a custom Docker."

RUN echo 'APT::Install-Suggests "0";' >> /etc/apt/apt.conf.d/00-docker
RUN echo 'APT::Install-Recommends "0";' >> /etc/apt/apt.conf.d/00-docker

# Disable Prompt During Packages Installation
ARG DEBIAN_FRONTEND=noninteractive
# Upadate
RUN apt-get update && \
 apt-get install openssh-server sudo -y && \
 apt-get install python3 sudo -y && \
 apt-get install python3-numpy sudo -y && \
 apt-get install nano sudo -y
 
RUN apt clean

RUN useradd -rm -d /home/ubuntu -s /bin/bash -g root -G sudo -u 1000 test

RUN echo 'test:test' | chpasswd

RUN service ssh start

# EXPOSE 22

# # ENTRYPOINT ["/bin/bash"]

# CMD ["/usr/sbin/sshd","-D"]
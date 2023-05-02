FROM ubuntu:20.04
ARG USER_PASSWORD
RUN apt-get update -y sudo
RUN apt-get -y install openssh-server openssh-clients
RUN echo "PasswordAuthentication yes" >> /etc/ssh/sshd_config
RUN ssh-keygen -A
RUN echo "root:${USER_PASSWORD}" | chpasswd
RUN apt-get install -y python3
RUN apt-get install wget -y sudo
RUN wget https://raw.githubusercontent.com/gdraheim/docker-systemctl-replacement/master/files/docker/systemctl3.py -O /usr/bin/systemctl
CMD ["/usr/sbin/sshd", "-D"]


FROM ubuntu:20.04
# ARG USER_PASSWORD
RUN apt-get update && \
    apt-get install -y openssh-server openssh-clients && \
    apt-get install -y python3 && \
    apt-get install nano sudo -y && \
    apt-get install curl sudo -y && \
    apt-get install software-properties-common sudo -y
# RUN echo "PasswordAuthentication yes" >> /etc/ssh/sshd_config
RUN mkdir /var/run/sshd
RUN echo 'root:password' | chpasswd
RUN sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN ssh-keygen -A
# RUN echo "root:${USER_PASSWORD}" | chpasswd
# RUN apt-get install python3 sudo -y
RUN apt-get install wget sudo -y
RUN wget https://raw.githubusercontent.com/gdraheim/docker-systemctl-replacement/master/files/docker/systemctl3.py -O /usr/bin/systemctl
CMD ["/usr/sbin/sshd", "-D"]


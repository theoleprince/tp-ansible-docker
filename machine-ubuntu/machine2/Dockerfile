FROM ubuntu:20.04
RUN apt-get update && \
    apt-get install -y openssh-server python3 && \
    apt-get install nano sudo -y && \
    apt-get install curl sudo -y && \
    apt-get install software-properties-common sudo -y
RUN mkdir /var/run/sshd
RUN echo 'root:password' | chpasswd
RUN sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config
EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]
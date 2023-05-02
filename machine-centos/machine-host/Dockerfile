FROM centos:centos7.9.2009
ARG USER_PASSWORD
RUN yum update -y
RUN yum -y install openssh-server openssh-clients
RUN echo "PasswordAuthentication yes" >> /etc/ssh/sshd_config
RUN ssh-keygen -A
RUN echo "root:${USER_PASSWORD}" | chpasswd
RUN yum install -y python3
RUN yum install wget -y
RUN wget https://raw.githubusercontent.com/gdraheim/docker-systemctl-replacement/master/files/docker/systemctl.py -O /usr/bin/systemctl
CMD ["/usr/sbin/sshd", "-D"]


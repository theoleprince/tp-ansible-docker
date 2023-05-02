FROM centos:centos7.9.2009
RUN mkdir -p /playbooks
RUN chmod 777 -R /playbooks
RUN yum update -y
RUN yum install epel-release -y
RUN yum install -y python3
RUN yum install ansible -y
RUN yum -y install openssh-clients
CMD tail -f /dev/null



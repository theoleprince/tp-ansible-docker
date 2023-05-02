FROM ubuntu:20.04
RUN mkdir -p /playbooks
RUN chmod 777 -R /playbooks
RUN apt-get update -y sudo
RUN apt-get install epel-release -y sudo
RUN apt-get install python3 -y sudo
RUN apt-get install ansible -y sudo
RUN apt-get install openssh-clients -y sudo
CMD tail -f /dev/null



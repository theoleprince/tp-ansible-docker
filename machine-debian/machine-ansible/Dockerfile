FROM ubuntu:20.04
RUN mkdir -p /playbooks
RUN chmod 777 -R /playbooks
RUN apt-get update && \
    apt-get install -y openssh-clients python3

    #  && \
    # apt-get install -y openssh-clients python3 && \
    # apt-get install nano sudo -y && \
    # apt-get install curl sudo -y && \
    # apt-get install software-properties-common sudo -y && \
    # apt-get install ansible sudo -y
CMD tail -f /dev/null



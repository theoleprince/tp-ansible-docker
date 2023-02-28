# image ubuntu version 20.04
FROM ubuntu:20.04
# Upadate
RUN apt-get update && apt-get install openssh-server sudo -y
# && apt-get install python3 && apt-get install python3-numpy && apt-get install nano && apt-get install openssh-server sudo -y

RUN useradd -rm -d /home/ubuntu -s /bin/bash -g root -G sudo -u 1000 test

RUN echo 'test:test' | chpasswd

RUN service ssh start

EXPOSE 22

# ENTRYPOINT ["/bin/bash"]

CMD ["/usr/sbin/sshd","-D"]
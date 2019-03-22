FROM ubuntu:18.04

RUN apt-get update

RUN apt-get install -y openssh-server python3
RUN mkdir /var/run/sshd

RUN apt-get clean

COPY authorized_keys /root/.ssh/authorized_keys

RUN ["chmod","0600","/root/.ssh/authorized_keys"]

EXPOSE 22

CMD    ["/usr/sbin/sshd", "-D"]

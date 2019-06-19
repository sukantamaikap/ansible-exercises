FROM ubuntu:18.04

EXPOSE 22 8088 50070

RUN apt-get -y update \
    && apt-get install -y \ 
    iputils-ping \
    openssh-server \
    && mkdir /var/run/sshd \
    && echo 'root:THEPASSWORDYOUCREATED' | chpasswd \
    && sed -i 's/PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config \
    && sed 's@session\s*required\s*pam_loginuid.so@session optional pam_loginuid.so@g' -i /etc/pam.d/sshd

ENV NOTVISIBLE "in users profile"
RUN echo "export VISIBLE=now" >> /etc/profile

# CMD service ssh start && while true; do sleep 3000; done
CMD ["/usr/sbin/sshd", "-D"]
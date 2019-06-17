FROM ubuntu:18.04

EXPOSE 22

RUN apt-get -y update \
    && apt install -y \ 
    ansible \
    iputils-ping \
    curl \
    openssh-client \
    && ansible --version

ENV ANSIBEL_CONFIG=/opt/sandbox/src/ansible.cfg

CMD ["/bin/bash"]
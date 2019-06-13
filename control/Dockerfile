FROM ubuntu:18.04

RUN apt-get -y update \
    && apt install -y \ 
    ansible \
    iputils-ping \
    curl \
    && ansible --version

ENV ANSIBEL_CONFIG=/opt/sandbox/src/ansible.cfg

CMD ["/bin/bash"]
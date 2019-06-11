FROM ubuntu:18.04

RUN apt-get -y update \
    && apt install -y \ 
    ansible \
    iputils \
    curl \
    && ansible --version

CMD ["/bin/bash"]
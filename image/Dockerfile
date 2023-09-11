FROM ubuntu:22.04

RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip \
    python3-dev \
    git \
    curl \
    wget \
    vim \
    nano \
    htop \
    iproute2 \
    sudo \
    screen \
    zsh \
    openssh-server && \
    rm -rf /var/lib/apt/lists/* && \
    mkdir /var/run/sshd

RUN python3 -m pip install --upgrade pip wheel setuptools && \
    python3 -m pip install --upgrade SNL2023f && \
    mkdir -p /opt/sparcs/newbie/seminar && \
    printf "You Found me!" > /opt/sparcs/newbie/seminar/findme && \
    printf "SPARCS\nSystem Programmers’ Association for Researching Computer Systems\n\nGeoul\nAra\nOTL\nZabo\nTaxi\nSSO\nBiseo\nMemvers\nWiki\n" > /sparcs && \
    chmod 644 /sparcs && \
    chmod 755 /opt/sparcs -R && \
    chmod 644 /opt/sparcs/newbie/seminar/findme


CMD ["sh", "-c", "python3 -m pip install -U snl2023f; /usr/local/bin/snl container"]

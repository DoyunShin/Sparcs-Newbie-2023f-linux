FROM ubuntu:22.04

RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip \
    python3-dev \
    git \
    curl \
    wget \
    vim \
    htop \
    iproute2 \
    sudo \
    openssh-server && \
    rm -rf /var/lib/apt/lists/* && \
    mkdir /var/run/sshd && \
    python3 -m pip install --upgrade pip wheel setuptools && \
    python3 -m pip install --upgrade SNL2023f

CMD ["python3 -m pip install --upgrade SNL2023f && python3 -m SNL2023f container"]

FROM --platform=arm64 ubuntu:21.10

RUN apt update -y && \
apt upgrade -y && \
apt install build-essential -y

RUN apt update -y && \
apt install -y curl wget git && \
wget https://nodejs.org/dist/v16.14.2/node-v16.14.2.tar.gz && \
tar -xzf node-v16.14.2.tar.gz -C /usr/local && \
rm -rf /var/lib/apt/lists/

RUN wget https://dl.google.com/go/go1.18.5.linux-amd64.tar.gz && \
tar -xzf go1.18.5.linux-amd64.tar.gz -C /usr/local

ENV PATH $PATH:/usr/local/go/bin

ADD ./apps /apps

EXPOSE 9090 3000 5432






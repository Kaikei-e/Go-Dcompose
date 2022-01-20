FROM ubuntu:20.10

RUN apt update -y && \
apt upgrade -y && \
apt install build-essential -y

RUN apt update -y && \
apt install -y curl wget git && \
curl -o nodejs.deb https://deb.nodesource.com/node_16.x/pool/main/n/nodejs/nodejs_16.13.0-deb-1nodesource1_amd64.deb && \
apt install -y ./nodejs.deb && \
rm nodejs.deb && \
rm -rf /var/lib/apt/lists/

RUN wget https://dl.google.com/go/go1.17.6.linux-amd64.tar.gz && \
tar -C /usr/local -xzf go1.17.6.linux-amd64.tar.gz

ENV PATH $PATH:/usr/local/go/bin

ADD ./apps /apps

EXPOSE 8080






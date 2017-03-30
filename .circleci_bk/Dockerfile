FROM debian

ENV DOCKER_VER 17.03.0-ce

RUN apt-get update && apt-get install -y \
    curl \
    --no-install-recommends && rm -rf /var/lib/apt/lists/*

RUN curl -k -L -o /tmp/docker-$DOCKER_VER.tgz https://get.docker.com/builds/Linux/x86_64/docker-$DOCKER_VER.tgz
RUN tar -xz -C /tmp -f /tmp/docker-$DOCKER_VER.tgz
RUN mv /tmp/docker/* /usr/bin

RUN curl -k -L https://github.com/docker/compose/releases/download/1.11.2/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
RUN chmod +x /usr/local/bin/docker-compose

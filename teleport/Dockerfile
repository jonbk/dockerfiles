FROM debian:bookworm-slim

RUN apt-get update && apt-get install -y \
    curl \
    && rm -rf /var/lib/apt/lists/*

RUN curl https://goteleport.com/static/install.sh | bash -s 13.3.5

RUN groupadd -g 1000 teleport \
    && useradd -l -u 1000 -g teleport -d /home/teleport -r teleport \
    && mkdir -p /home/teleport/app \
    && chown -R 1000:1000 /home/teleport

USER teleport

WORKDIR /home/teleport/app
FROM jenkins

USER root

# Install more tools
RUN apt-get update \
  && apt-get install -y --no-install-recommends \
    docker \
    sudo \
    jq \
    rsync \
  && rm -rf /var/lib/apt/lists/*

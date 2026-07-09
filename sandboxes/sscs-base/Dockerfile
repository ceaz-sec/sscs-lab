FROM debian:bookworm-slim

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        bash \
        ca-certificates \
        curl \
        wget \
        git \
        jq \
        ripgrep \
        fd-find \
        file \
        vim-common \
        neovim \
        tcpdump \
        tshark \
        yara \
        hexyl \
        binwalk \
        diffoscope \
        unzip \
        xz-utils && \
    rm -rf /var/lib/apt/lists/*

# Syft
RUN curl -sSfL https://raw.githubusercontent.com/anchore/syft/main/install.sh \
    | sh -s -- -b /usr/local/bin

# Grype
RUN curl -sSfL https://raw.githubusercontent.com/anchore/grype/main/install.sh \
    | sh -s -- -b /usr/local/bin

WORKDIR /workspace

CMD ["/bin/bash"]

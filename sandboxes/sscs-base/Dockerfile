FROM alpine:latest

RUN apk add --no-cache \
        bash \
        ca-certificates \
        curl \
        wget \
        git \
        jq \
        ripgrep \
        tar \
        fd \
        file \
        vim \
        neovim \
        tcpdump \
        tshark \
        yara \
        hexyl \
        unzip \
        xz \
        shadow

# Scorecard
ARG SCORECARD_VERSION=5.0.0

RUN curl -L "https://github.com/ossf/scorecard/releases/download/v${SCORECARD_VERSION}/scorecard_${SCORECARD_VERSION}_linux_amd64.tar.gz" -o scorecard.tar.gz \
    && tar -xzf scorecard.tar.gz \
    && mv scorecard-linux-amd64 /usr/local/bin/scorecard \
    && rm scorecard.tar.gz

# Syft
RUN curl -sSfL https://raw.githubusercontent.com/anchore/syft/main/install.sh \
    | sh -s -- -b /usr/local/bin

# Grype
RUN curl -sSfL https://raw.githubusercontent.com/anchore/grype/main/install.sh \
    | sh -s -- -b /usr/local/bin

RUN useradd -m -u 1000 devsec

WORKDIR /workspace
CMD ["/bin/bash"]

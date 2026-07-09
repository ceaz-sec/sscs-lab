FROM sscs-base
USER root
RUN apk add --no-cache build-base
USER devsec
RUN curl https://sh.rustup.rs -sSf | sh -s -- -y
ENV PATH="/home/devsec/.cargo/bin:${PATH}"
RUN cargo install \
        cargo-audit \
        cargo-deny
WORKDIR /home/devsec/workspace

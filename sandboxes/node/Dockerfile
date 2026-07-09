FROM sscs-base

RUN curl -fsSL https://deb.nodesource.com/setup_lts.x | bash - && \
    apt-get update && \
    apt-get install -y nodejs && \
    npm install -g pnpm

WORKDIR /workspace

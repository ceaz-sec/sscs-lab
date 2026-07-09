FROM sscs-base

RUN wget https://go.dev/dl/go1.25.0.linux-amd64.tar.gz && \
    tar -C /usr/local -xzf go1.25.0.linux-amd64.tar.gz && \
    rm go1.25.0.linux-amd64.tar.gz

ENV PATH="/usr/local/go/bin:${PATH}"

RUN go install golang.org/x/vuln/cmd/govulncheck@latest && \
    go install github.com/securego/gosec/v2/cmd/gosec@latest

ENV PATH="/root/go/bin:${PATH}"

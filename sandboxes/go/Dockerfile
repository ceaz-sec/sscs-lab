FROM sscs-base
USER root
RUN apk add --no-cache go
ENV PATH="/usr/local/go/bin:/home/devsec/go/bin:${PATH}"
RUN go install golang.org/x/vuln/cmd/govulncheck@latest && \
    go install github.com/securego/gosec/v2/cmd/gosec@latest
USER devsec
WORKDIR /home/devsec/workspace

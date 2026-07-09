FROM sscs-base
USER root
RUN apk add --no-cache nodejs npm
USER devsec
ENV NPM_CONFIG_PREFIX=/home/devsec/.npm-global
ENV PATH="/home/devsec/.npm-global/bin:${PATH}"
RUN npm install -g \
        pnpm \
        npm-check-updates
WORKDIR /home/devsec/workspace

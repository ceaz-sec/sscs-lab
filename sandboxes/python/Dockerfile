FROM sscs-base
USER root
RUN apk add --no-cache python3 py3-pip build-base
USER devsec
ENV PATH="/home/devsec/.local/bin:${PATH}"
RUN pip install --user --break-system-packages \
        pip-audit \
        pipenv
WORKDIR /home/devsec/workspace

FROM sscs-base

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        python3 \
        python3-pip \
        pipx \
        python3-venv && \
    rm -rf /var/lib/apt/lists/*

ENV PATH="/root/.local/bin:${PATH}"

RUN pipx install uv && \
    pipx install ruff && \
    pipx install bandit && \
    pipx install pip-audit

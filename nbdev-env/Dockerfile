FROM python:3.10.4-slim-bullseye

ARG GID=1000
ARG UID=1000

RUN addgroup --gid=$GID loper && adduser --uid=$UID --gid=$GID loper && \
    apt-get update && apt-get install -y --no-install-recommends ruby-full build-essential git && \
    rm -rf /var/lib/apt/lists/*

USER loper
ENV HOME=/home/loper
ENV GEM_HOME=$HOME/.local/gems
ENV PATH=$GEM_HOME/bin:$PATH
ENV PATH=$HOME/.local/bin:$PATH
ENV PIP_CACHE_DIR=$HOME/.cache/pip

WORKDIR /home/loper
COPY --chown=$GID:$UID ./nbdev-env/requirements.txt requirements.txt

SHELL ["/bin/bash", "-c"]

RUN gem install jekyll bundler && \
    pip install --user --upgrade pip && \
    pip install --user --upgrade --requirement requirements.txt

VOLUME /home/loper

CMD ["env"]

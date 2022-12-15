FROM jupyter/pyspark-notebook

USER root

ENV DEBIAN_FRONTEND=noninteractive
RUN apt update && apt install -y curl gh && rm -rf /var/lib/apt/lists/*

### install quarto
# versions: https://quarto.org/docs/download/_download.json
RUN curl --silent -L --fail \
        https://github.com/quarto-dev/quarto-cli/releases/download/v1.2.269/quarto-1.2.269-linux-amd64.deb > /tmp/quarto.deb && \
    apt update && \
    apt install -y --no-install-recommends /tmp/quarto.deb

USER ${NB_UID}
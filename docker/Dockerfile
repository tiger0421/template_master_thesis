FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update --quiet \
    && apt upgrade --quiet -y \
    && apt install --quiet --no-install-recommends -y \
        texlive-full \
        texlive-fonts-recommended \
        texlive-fonts-extra \
        texlive-lang-cjk \
        xdvik-ja \
    && apt clean \
    && apt autoremove -y \
    && rm -rf /var/lib/apt/lists/*

RUN apt update --quiet \
    && apt install --quiet --no-install-recommends -y \
        npm \
    && npm init -y \
    && npm install --global \
        textlint \
    && textlint --init \
    && npm cache clean --force \
    && apt clean \
    && apt autoremove -y \
    && rm -rf /var/lib/apt/lists/*

RUN apt update --quiet \
    && apt install --quiet --no-install-recommends -y \
        git \
    && apt clean \
    && apt autoremove -y \
    && rm -rf /var/lib/apt/lists/*

CMD ["/bin/bash"]

